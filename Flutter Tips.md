## Flutter Tips

1.FAB  at center

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



