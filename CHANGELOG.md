## 0.0.2

By this package you can search an item from the dropdown item list.
And also can get the input from TextField that not present in the dropdown items.

###Platforms
This widget has been successfully tested on iOS, Android and Chrome.

###Examples
<a href="https://github.com/SujitSarkar/Flutter-Dropdown-Search">example project available in the repository.</a>

###Screenshots
<a href="https://github.com/SujitSarkar/Flutter-Dropdown-Search/blob/master/ex_img/sc_1.png">Screenshot 1.</a>
<a href="https://github.com/SujitSarkar/Flutter-Dropdown-Search/blob/master/ex_img/sc_2.png">Screenshot 2.</a>

###Code
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
  TextEditingController _controller=TextEditingController();
  List<String> items=["Afghanistan", "Albania", "Algeria", "American Samoa",
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





