# paging

A Flutter package for paginating a list view

[![](https://flutter.zaynjarvis.com/version/paging)](https://pub.dartlang.org/packages/paging)
[![](https://flutter.zaynjarvis.com/score/paging)](https://pub.dartlang.org/packages/paging)

## Installation

Add this to your package's pubspec.yaml file

```yaml
dependencies:
  ...
  paging: ^latest.version.here
```

## Usage
First import paging.dart

```dart
  import 'package:paging/paging.dart';
```
Simple to use. You can pass a type \<T\> as a parameter to the widget, by default dynamic is assumed.

There are two required parameters:
- pageBuilder: requires a Future of List\<T\> and gives you the current size of list
- itemBuilder: requires a widget and gives you the item of type \<T\> to be displayed

```dart
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text('Pagination List')),
      body: Pagination<String>(
        pageBuilder: (currentSize) => pageData(currentSize),
        itemBuilder: (item){
          return Container(
                    color: Colors.yellow,
                    height: 48,
                    child: Text(item),
                 );
        },
      ),
    );
  }
```

## Screenshots

<image src="./example_screen1.gif" width="200px"/>

## Getting Started

This project is a starting point for a Dart
[package](https://flutter.io/developing-packages/),
a library module containing code that can be shared easily across
multiple Flutter or Dart projects.

For help getting started with Flutter, view our 
[online documentation](https://flutter.io/docs), which offers tutorials, 
samples, guidance on mobile development, and a full API reference.
