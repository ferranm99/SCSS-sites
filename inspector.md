---
layout: page
title: Flutter Widget Inspector

permalink: /inspector/
---

The Flutter Widget Inspector is powerful tool for visualizing and exploring
Flutter widget trees.

* TOC Placeholder
{:toc}

## Flutter Widget Inspector

The Flutter framework uses widgets as [the core building
block](https://flutter.io/widgets-intro/) for anything from controls (text,
buttons, toggles, etc.) to layout (centering, padding, rows, columns, etc.).
The Inspector is powerful tool for visualizing and exploring Flutter
these widget trees. It can be helpful when:

* Undestanding existing layouts
* Diagnosing layout issues

![IntelliJ Flutter Inspector Window](/images/intellij/visual-debugging.png)

To start click "Select widget" on the Flutter Inspector toolbar and then click
on the device to select a widget. The selected widget will then be highlighted
on the device and in the widget tree.
![Select Demo](/images/intellij/inspector_select_example.gif)

You can then browse around the interactive widget tree in the IDE to view
nearby widgets and see their field values. If you are trying to debug a layout
issue, then the Widgets layer’s tree may be insufficiently detailed. In that
case click on the Render Tree tab to view the render tree corresponding to the
same location in the tree. When debugging layout issues, the key fields to look
at are the `size` and `constraints` fields. The constraints flow down the tree,
and the sizes flow back up.

![Switch Trees](/images/intellij/switch_inspector_tree.gif)

For a more complete demonstration of the Inspector, please see the recent
[DartConf talk](https://www.youtube.com/watch?v=JIcmJNT9DNI).

## Get Started with the Inspector

The Inspector is currently available in [the Flutter plugin](/get-started/editor/)
for Android Studio, or IntelliJ IDEA.

## Feedback issues

If you have suggestions, or encounter issues, please
[file an issue in our tracker](https://github.com/flutter/flutter-intellij/issues/new?labels=inspector)!
