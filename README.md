# flutter_dropdown_search
By this package you can search an item from the dropdown item list.
And also can get the input from TextField that not present in the dropdown items.

## Getting Started
### Platforms
This widget has been successfully tested on iOS, Android and Chrome.

## Screenshots
| Outlook                        | Searching with country name    |
|--------------------------------|--------------------------------|
| ![image info](ex_img/sc_1.png) | ![image info](ex_img/sc_2.png) | 

## Code
```dart
import 'package:flutter/material.dart';
import 'package:flutter_dropdown_search/flutter_dropdown_search.dart';
void main() {
  runApp(MyApp());
}
class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
            title: 'Flutter Dropdown Search',
            theme: ThemeData(
              primarySwatch: Colors.blue,
            ),
            home: HomePage()
    );
  }
}
class HomePage extends StatelessWidget {
  final TextEditingController _controller=TextEditingController();
  final List<String> items=["Afghanistan", "Albania", "Algeria", "American Samoa",
    "Andorra", "Angola", "Anguilla", "Antarctica", "Antigua and Barbuda",
    "Argentina", "Armenia", "Aruba", "Australia", "Austria", "Azerbaijan"];
  
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Flutter Dropdown Search'),
      ),
      body: Padding(
        padding: EdgeInsets.symmetric(horizontal: 15,vertical: 20),
        child: Column(
          children: [
            FlutterDropdownSearch(
              textController: _controller,
              items: items,
              dropdownHeight: 300,
            )
          ],
        ),
      ),
    );
  }
}
```