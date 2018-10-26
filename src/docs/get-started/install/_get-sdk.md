{% if os == 'linux' -%}
  {% assign unzip = 'tar xf' -%}
  {% assign file_ext = '.tar.xz' -%}
{% else -%}
  {% assign unzip = 'unzip' -%}
  {% assign file_ext = '.zip' -%}
{% endif -%}

## Get the Flutter SDK {#get-sdk}

 1. Download the following installation bundle to get the latest beta release of the
    Flutter SDK:

    [(loading...)](#){:.download-latest-link-{{os}}.btn.btn-primary}

    For other release channels, and older builds, see the [SDK
    archive](/docs/development/tools/sdk/archive) page.
 1. Extract the file in the desired location, for example:

    {% comment %}
      Our JS also updates the filename in this template, but it doesn't include the terminal formatting:

      {% prettify shell %}
      $ cd ~/development
      $ {{unzip}} ~/Downloads/[[download-latest-link-filename]]flutter_{{os}}_vX.X.X-beta{{file_ext}}[[/end]]
      {% endprettify %}
    {% endcomment -%}

    ```terminal
    $ cd ~/development
    $ {{unzip}} ~/Downloads/flutter_{{os}}_vX.X.X-beta{{file_ext}}
    ```

 1. Add the `flutter` tool to your path:

    ```terminal
    $ export PATH=$PATH:`pwd`/flutter/bin
    ```

The above command sets your `PATH` variable temporarily, for the current terminal
window. To permanently add Flutter to your path, see [Update your
path](#update-your-path).

You are now ready to run Flutter commands!

To update an existing version of Flutter, see [Upgrading Flutter](/docs/development/tools/sdk/upgrading).

### Run flutter doctor

Run the following command to see if there are any dependencies you need to
install to complete the setup:

```terminal
$ flutter doctor [-v]
```

This command checks your environment and displays a report to the terminal
window. The Dart SDK is bundled with Flutter; it is not necessary to install
Dart separately. Check the output carefully for other software you may need to
install or further tasks to perform (shown in **bold** text).

For example:

<pre>
[-] Android toolchain - develop for Android devices
    • Android SDK at /Users/obiwan/Library/Android/sdk
    <strong>✗ Android SDK is missing command line tools; download from https://goo.gl/XxQghQ</strong>
    • Try re-installing or updating your Android SDK,
      visit https://flutter.io/setup/#android-setup for detailed instructions.
</pre>

The following sections describe how to perform these tasks and finish the setup
process.

Once you have installed any missing dependencies, run the `flutter doctor`
command again to verify that you’ve set everything up correctly.

{% include_relative _analytics.md %}
