# Flutter Tips

**Hey** **Coders** 🤓 ,

Welcome to flutter tips,

Here I m going to add Flutter snippets  which are useful,

although yes we can google and all but instead I want it all at one place,

So as I'm Going to learn I'm Going to update this page.

So Enjoy Flutter Guys !!





### FAB  at center

```dart
class ContaPage extends StatelessWidget {
  @override
  Widget build(BuildContext context) => new Scaffold(
    // ...

    floatingActionButton: new FloatingActionButton(
      // ...FloatingActionButton properties...
    ),

    // Here's the new attribute:

    floatingActionButtonLocation: FloatingActionButtonLocation.centerFloat,
  );
}
```

### FAB background Color

```dart
   floatingActionButton: FloatingActionButton(
        onPressed: () {
          // Add your onPressed code here!
        },
        child: Container(
          width: 60,
          height: 60,
          child: Icon(
            Icons.add,
          ),
          decoration: new BoxDecoration(
            shape: BoxShape.circle,
            gradient: new RadialGradient(
              colors: [Colors.orange, Color(0xFFF500).withOpacity(0.5)],
                //opacity for transparent
            ),
          ),
        ),
      ),
```



### Decoration common code:

```dART
         //Applied in container
         
         decoration: new BoxDecoration(
            shape: BoxShape.circle,
             //this is radialgradient
            gradient: new RadialGradient(
              colors: [Colors.orange, Color(0xFFF500).withOpacity(0.5)],
                //opacity for transparent
            ),
          ),
```



### Decoration Gradient Color

Reference for extra:[Gradient](https://owenhalliday.co.uk/flutter-gradient/)

```dart
      body: Container(
        decoration: BoxDecoration(
          gradient: LinearGradient(
              //provide begin and end
              begin: Alignment(6.123234262925839e-17, 1),
              end: Alignment(-1, 6.123234262925839e-17),
              //Optional u can use this too
                begin: Alignment.topLeft,//well it is preferred method
      			end: Alignment.bottomRight,
      			stops: [0.3, 1],//it manages how much color to extend
              
              colors: [
                  //Provide Colors here
                Color.fromRGBO(69, 182, 73, 1),
                Color.fromRGBO(46, 196, 182, 1)
              ]),
        ),
```



### Show ModalBottomSheet halfScreen Popup:

```dart
      onPressed: () {
          //Starts here 
          showModalBottomSheet<void>(
            context: context,
            builder: (BuildContext context) {
              return Container(
                height: 200,
                color: Colors.amber,
                child: Center(
                  child: Column(
                    mainAxisAlignment: MainAxisAlignment.center,
                    mainAxisSize: MainAxisSize.min,
                    children: <Widget>[
                        //can add childrens here
                      const Text('Modal BottomSheet'),
                    ],
                  ),
                ),
              );
            },
          );
        },
```

### Border Radius

```dart
decoration: BoxDecoration(
                  borderRadius: BorderRadius.only(
                      //many methods are there like
                      //borderRadius.all(),..etc..
                      topLeft: Radius.circular(25),
                      topRight: Radius.circular(25)),

)
```

### Important Modal Bottom Sheet points:

#### In Bottom Sheet if we apply radius it may show white color at background

###### So 2 Solutions :

###### 1.Override 

```dart
 showModalBottomSheet<void>(
            backgroundColor: Colors.transparent,
            ......
            .
            //Bottom Sheet code
```

###### 2.Set Theme

```dart
MaterialApp(
    theme: ThemeData(
      // Draw all modals with a white background and top rounded corners
      bottomSheetTheme: BottomSheetThemeData(
        backgroundColor: Colors.white,
          //change background color here or try transparent
        shape: RoundedRectangleBorder(
          borderRadius: BorderRadius.vertical(top: Radius.circular(10))
        )
      )
    ),
```

### Use Google Font

```dart
//import
import 'package:google_fonts/google_fonts.dart';


//This is override method which I like
 Text('What made you Happy today?',
     style:
    GoogleFonts.alice(color: Colors.white, fontSize: 18),
   //Change alice with preffered font
     ),
```

### Add Space Box (Empty Space)

```dart
SizedBox(height: 80)
//You can use it with childrens or two buttons and many..

```

