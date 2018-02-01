---
layout: page
title: Learn Flutter; rendering widgets with build()

permalink: /learn/build/
---

This page teaches the basic concept of how widgets are rendered.

* Placeholder for TOC
{:toc}

## Widgets

All rendering in Flutter is performed by widgets. Some widgets correspond to ‘controls’, for example `FlatButton` and `Text`. Other widgets control the layout of other Widgets, for example `Center` and `Row`.

## build() methods

Widgets ‘put pixels on the screen’ using a build() method. This method is called by the Flutter framework when the widget is part of the current rendering tree, and when any of the dependencies of the widget change.

Build methods often render content by instantiating other widgets. Actually, this is a very common pattern in Flutter: Widgets are rendered by composing them from existing widgets. As a concrete example, consider the build() method of the app you just created after the installation step:

```dart
Widget build(BuildContext context) {
  return new MaterialApp(
    title: 'Flutter Demo',
    home: new Scaffold(
      appBar: new AppBar(
        title: new Text('Android'),
      ),
      body: new Center(
        child: new Text('Hello World'),
      ),
    ),
  );
}
```

This starts by instantiating a new MaterialApp; a widget that contains a full skeleton of a mobile application usign Material design. This app is configured with a 'scaffold', and this is in turn configured with an application bar, and a body, again by creating new widgets.

Try to change some of the text strings in the source code, and hit hot reload to see the effect of the change!

## Next step

Now that you understand the basics of rendering a widget with build(), let’s move on to [rendering widgets that contain state](/learn/state/).
