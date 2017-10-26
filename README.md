## A port of git new-workdir to support submodules

The main git repo includes contrib/workdir/, which is a command that
allows sharing objects in the .git/ folder between repos.  This is
useful on jenkins and other platforms where you might have the same
repo checked out in several different directories.

Newer versions of git have added support for this functionality in a
different way, via GIT_ALTERNATE_OBJECT_DIRECTORIES.  But it doesn't
work very well with submodules.  Neither does the original
git-workdir.  But this version does!
