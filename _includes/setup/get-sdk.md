## Get the Flutter SDK

To get Flutter, use `git` to clone the repository and then add the `flutter` tool to your path.
Running `flutter doctor` shows any remaining dependencies you may need to install.

### Clone the repo

If this is the first time you're installing Flutter on this machine, clone the
alpha branch of the repository and then add the `flutter` tool to your path:

```
$ git clone -b alpha https://github.com/flutter/flutter.git
$ export PATH=`pwd`/flutter/bin:$PATH
```
The above command sets your PATH variable temporarily, for the current terminal window. To
permanently add Flutter to your path, see [Update your path](#update-your-path).

To update an existing version of Flutter, see [Upgrading Flutter](/upgrading/).


### Run flutter doctor

Run the following command to see if there are any dependencies you need to install to complete
the setup:

```
$ flutter doctor
```

This command checks your environment and displays a report to the terminal window.
The Dart SDK is bundled with Flutter; it is not necessary to install Dart separately.
Check the output carefully for other software you may need to install or further 
tasks to perform (shown in **bold** text).

For example:
```
✗ Xcode end user license agreement not signed; open Xcode or run the command 'sudo xcodebuild -license'.

✗ Brew not installed; use this to install tools for iOS device development.

  Download brew at http://brew.sh/.
```

The first time you run the `flutter` command, it downloads its own dependencies and compiles
itself. Subsequent runs should be much faster.

The following sections describe how to perform these tasks and finish the setup process.
You'll see in `flutter doctor` output that if you choose to use an IDE, plugins
are available for IntelliJ IDEA. See [IntelliJ Setup](/intellij-setup/)
for the steps to install the Flutter and Dart plugins.

Once you have installed any missing dependencies, run the `flutter doctor` command again to
verify that you’ve set everything up correctly.

The `flutter` tool uses Google Analytics to anonymously report feature usage statistics
and basic crash reports. This data is used to help improve Flutter tools over time.
Analytics is not sent on the very first run or for any runs involving `flutter config`,
so you can opt out of analytics before any data is sent. To disable reporting, 
type `flutter config --no-analytics` and to display the current setting, type 
`flutter config`. See Google's privacy policy:[www.google.com/intl/en/policies/privacy](https://www.google.com/intl/en/policies/privacy/).
{: .alert-warning}
