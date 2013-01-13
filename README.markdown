Diff, Match and Patch Library, Objective C port
===============================================

<http://code.google.com/p/google-diff-match-patch/>

## Diff, Match and Patch library for plain text

The Diff Match and Patch libraries offer robust algorithms to perform
the operations required for synchronizing plain text.

### Diff:

-   Compare two blocks of plain text and efficiently return a list of
    differences.
-   [Diff
    Demo](http://neil.fraser.name/software/diff_match_patch/svn/trunk/demos/demo_diff.html)

### Match:

-   Given a search string, find its best fuzzy match in a block of plain
    text. Weighted for both accuracy and location.
-   [Match
    Demo](http://neil.fraser.name/software/diff_match_patch/svn/trunk/demos/demo_match.html)

### Patch:

-   Apply a list of patches onto plain text. Use best-effort to apply
    patch even when the underlying text doesn't match.
-   [Patch
    Demo](http://neil.fraser.name/software/diff_match_patch/svn/trunk/demos/demo_patch.html)

Currently available in Java, JavaScript, Dart, C++, C\#, Objective C,
Lua and Python. Regardless of language, each library features [the same
API](http://code.google.com/p/google-diff-match-patch/wiki/API) and the
same functionality. All versions also have comprehensive test harnesses.

### Algorithms

This library implements [Myer's diff
algorithm](http://neil.fraser.name/software/diff_match_patch/myers.pdf)
which is generally considered to be the best general-purpose diff. A
layer of [pre-diff speedups and post-diff
cleanups](http://neil.fraser.name/writing/diff/) surround the diff
algorithm, improving both performance and output quality.

This library also implements a [Bitap matching
algorithm](http://neil.fraser.name/software/diff_match_patch/bitap.ps)
at the heart of a flexible [matching and patching
strategy](http://neil.fraser.name/writing/patch/).

Usage
-----

Add “DiffMatchPatch.xcodeproj” to your project (preferably into “Frameworks” to keep things tidy).

In your target’s “Build Phases”:

* Add Build Phase (+-button pull-down menu) > Copy Files
* Destination: Frameworks
* Change name to “Copy Frameworks” to keep things clean

Add “DiffMatchPatch.framework” to the following build phases (via the +-buttons):

* “Target Dependencies”
* “Link Binary With Libraries”
* “Copy Frameworks” (created above)

And finally add the header to your code:

    #import <DiffMatchPatch/DiffMatchPatch.h>


Notes
-----

If you want to run the speed test, you first need to change the working directory of the executable “speedtest” to “Project directory”. This cannot be done beforehand, because this setting is stored in the current user’s project settings. 