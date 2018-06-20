---
layout: page
title: "Adding Material Touch Ripples"
permalink: /cookbook/gestures/ripples/
---

While designing an app that should follow the Material Design Guidelines, we'll 
want to add the ripple animation to Widgets when tapped. 

Flutter provides the [`InkWell`](https://docs.flutter.io/flutter/material/InkWell-class.html)
Widget to achieve this effect.

## Directions

  1. Create a Widget we want to tap
  2. Wrap it in an `InkWell` Widget to manage tap callbacks and ripple animations 
 
<!-- skip -->
```dart
// The InkWell Wraps our custom flat button Widget
InkWell(
  // When the user taps the button, show a snackbar
  onTap: () {
    Scaffold.of(context).showSnackBar(SnackBar(
      content: Text('Tap'),
    ));
  },
  child: Container(
    padding: EdgeInsets.all(12.0),
    child: Text('Flat Button'),
  ),
);
```   

## Complete example

```dart
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    final title = 'InkWell Demo';

    return MaterialApp(
      title: title,
      home: MyHomePage(title: title),
    );
  }
}

class MyHomePage extends StatelessWidget {
  final String title;

  MyHomePage({Key key, this.title}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(title),
      ),
      body: Center(child: MyButton()),
    );
  }
}

class MyButton extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    // The InkWell Wraps our custom flat button Widget
    return InkWell(
      // When the user taps the button, show a snackbar
      onTap: () {
        Scaffold.of(context).showSnackBar(SnackBar(
              content: Text('Tap'),
            ));
      },
      child: Container(
        padding: EdgeInsets.all(12.0),
        child: Text('Flat Button'),
      ),
    );
  }
}
```

![Ripples Demo](/images/cookbook/ripples.gif)
