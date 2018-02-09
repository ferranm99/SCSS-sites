---
layout: page
title: Getting started with your first Flutter app

permalink: /getting-started/
---

This page describes how to create and run your first Flutter app.

{% include note.html content="The Flutter SDK is a prerequisite for the tasks on this page. 
Make sure you [install the Flutter SDK](/setup/) before continuing." %}

* Placeholder for TOC
{:toc}

## Creating your first Flutter app

To create a starter project, open a terminal and run the `flutter create <project name>` command .

Here is an example:

{% commandline %}
flutter create myapp
{% endcommandline %}

The above command creates a Flutter project directory called `myapp` that contains a simple demo
app that uses [Material Design](https://www.google.com/design/spec/material-design/introduction.html).

In the project directory, the code for your app is in `myapp/lib/main.dart`.

## Running your Flutter app

Use the `flutter run` command to run your Flutter app on a connected
device or simulator.

To run your app from the command-line:

1. Open a terminal and change directories to the root of your app (the same directory that
contains the `pubspec.yaml` file for your project).
2. Run the following command. Once the `flutter` tool is running, if you change the app's
source code, you can hit `r` to hot-reload your application (updating the source on the fly
without actually restarting the entire app).

{% commandline %}
cd myapp
flutter run
{% endcommandline %}


If more than one device is connected, use the `flutter devices` command
to get their IDs, and then `flutter run -d deviceID` to run your app.

Alternatively, if you are using the [IntelliJ
IDEA](https://www.jetbrains.com/idea/) IDE (either the free Community Edition, or the
Ultimate Edition) with the [Flutter
plugins](/ide-setup/), you can start your Flutter app from there:

1. In IntelliJ, click **Create New Project** from the Welcome window or
**File > New > Project...** from the main IDE window.
1. Select **Flutter** in the menu, and click **Next**.
1. Under **Project location** enter, or browse to, the directory holding your new Flutter app.
1. Click **Finish**.
1. Click the **Run icon** in the toolbar, or invoke the menu item **Run > Run**.

![Main IntelliJ toolbar](/images/intellij/main-toolbar.png)

*Note*: If the Run & Debug buttons are disabled, and no targets are listed, Flutter
has not been able to discover any connected iOS or Android devices or simulators.
You need to connect a device, or start a simulator, to proceed.

If everything works, you should see your starter app on your device or simulator.

<div id="starter-app-screenshots">
  <figure style='display: inline-block'>
    <img src="/images/flutter-starter-app-ios.png" alt="Starter App on iOS">
    <figcaption>Figure 1. iOS (iPhone 6s Plus)</figcaption>
  </figure>
  <figure style='display: inline-block'>
    <img src="/images/flutter-starter-app-android.png" alt="Starter App on Android">
    <figcaption>Figure 2. Android (Nexus 6P)</figcaption>
  </figure>
</div>

## Quickly viewing source code changes with 'hot reload'

Flutter offers a fast development cycle with _hot reload_,
the ability to reload the code of a live running app
without restarting or losing app state. Simply make a
change to your source code, tell your IDE or command-line
tool that you want to hot reload, and see the change
in your simulator, emulator, or device.

![Hot reload in IntelliJ](/images/intellij/hot-reload.gif)

To edit your code and hot reload changes:

1. Start your app with 'Run' (without breakpoints) or 'Debug' (with breakpoints).
1. Make desired changes in your source code.
1. Do not press the 'Stop' button; let your app continue to run.
1. To see your changes invoke **Save All** (`cmd-s` / `ctrl-s`),
   or click the **Hot Reload button** (the button with the lightning bolt icon).

A more detailed description on how to use the IntelliJ plugin and which
changes are supported by the hot reload feature can be found on the page
[Developing apps in the IntelliJ IDE](../using-ide/).

## Next steps

Please reach out to us at our [mailing list][mailinglist]. We'd love
to hear from you!

You might also want to check out:
* [Building Beautiful UIs with Flutter - Codelab](https://codelabs.developers.google.com/codelabs/flutter/index.html#0)
* [Introduction to Flutter's Widget Framework](/widgets-intro/)

Happy Fluttering!


[mailinglist]: mailto:flutter-dev@googlegroups.com
