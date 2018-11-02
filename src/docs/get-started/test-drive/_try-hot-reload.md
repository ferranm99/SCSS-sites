After the app build completes, you'll see the starter app on your device.

{% include app-figure.md img-class="site-mobile-screenshot border" image="starter-app.png" caption="Starter app" platform="iOS" %}

## Try hot reload

Flutter offers a fast development cycle with _hot reload_, the ability to reload
the code of a live running app without restarting or losing app state.
Make a change to app source, tell your IDE or command-line tool that you
want to hot reload, and see the change in your simulator, emulator, or device.

 1. Open `lib/main.dart`.
 1. Change the string
    <code class="text-nowrap">
    'You have <del>pushed</del> the button this many times'
    </code>
    to
    <code class="text-nowrap">
      'You have <ins>clicked</ins> the button this many times'
    </code>.

    {{site.alert.important}}
      Do _not_ press the **Stop** button; let your app run.
    {{site.alert.end}}

 1. Save your changes{{include.save_changes}}

You'll see the updated string in the running app almost immediately.
