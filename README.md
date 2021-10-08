# flutterInterview

```dart



@override
Widget build(BuildContext context) {
  
  RandomProvider randomProvider = Provider.of<RandomProvider>(context, listen: false);
  String buttonText = randomProvider.buttonText;
  
  return Center(
    child: GestureDetector(
      onTap: (){
        randomProvider.buttonText = "Clicked";
        setState((){});
      },
      child: Container(
        width = 300,
        height = 100,
        child: Text('$buttonText'),
      ),
    ),
  );
}
