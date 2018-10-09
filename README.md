# kdev-clang-tidy

A plugin for [KDevelop](https://www.kdevelop.org) to support [Clang-Tidy](http://clang.llvm.org/extra/clang-tidy/) static analysis.

The last stand-alone release is 0.3.3.

**NOTE:**
Since then kdev-clang-tidy has been moved into kdevelop.git:plugins/clangtidy and will be released as part of KDevelop, starting with KDevelop 5.4.

## Get It For KDevelop 5.2/5.3

Search the package manager of your Linux distribution or *BSD system for it (e.g. kdevelop-clang-tidy or kdev-clang-tidy):

* Arch Linux: kdevelop-clang-tidy
* Gentoo: kdevelop-clang-tidy
* openSUSE: kdevelop5-plugin-clang-tidy
* (please report the name in your package system/distribution, so it can be listed here).

Or try to install it via its [AppStream Id Link](appstream://org.kde.kdev-clang-tidy)


## Use It

Once installed, open the global KDevelop settings: ensure in the "Plugins" page that the "Clang-Tidy Support" plugin is enabled, then in the "Analyzers"/"Clang-Tidy" page make sure the clang-tidy executable path points to an existing executable.

Next open the configuration dialog for a project and check the settings in the "Clang-Tidy" page.

Then open a C++ source file of your project. Now invoke a run of clang-tidy either via the main menu "Code"/"Analyze Current File With"/"Analyze Current File With Clang-Tidy" or via the context menu on the file "Analyze Current File With"/"Clang-Tidy". A job should be started and, once finished, the "Problems" tool view should show up with the page "Clang-Tidy" selected, listing the result of the run.

**NOTE:**
For now one has to enable oneself the creation of the so-called compilation database which clang-tidy uses, e.g. with CMake to set the flag         `CMAKE_EXPORT_COMPILE_COMMANDS` to `ON`
in the settings (listed under "Advanced values" in the project's CMake settings in KDevelop). The plugin does not (yet) handle that for you.


## Report Bugs & Feature Requests

Tell what issues you have or would like to see at the [KDE bug tracker, product "KDevelop", component "Analyzer: Clang-Tidy"](https://bugs.kde.org/enter_bug.cgi?format=guided&amp;product=kdevelop&amp;component=Analyzer:%20Clang-Tidy)
