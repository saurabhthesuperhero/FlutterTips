# Flutter Tips

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

