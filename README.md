# sort-xcodeproj

Script to sort "children" and "files" sections in Xcode project.pbxproj files. This script is lightly modified [the version](https://github.com/WebKit/webkit/blob/master/Tools/Scripts/sort-Xcode-project-file) found in Apple's WebKit repository. This version adds a `--check` flag, which only checks if the project file is sorted. `--check` makes this script suitible for use in commit hooks and CI.

## Usage

```
perl sort.pl [options] list of projects...
```

Example usage
```
$ perl sort.pl --check TestApp.xcodeproj
Projects must be sorted in --check mode at sort.pl line 123, <IN> line 208.
$ echo $?
25
```

## Extras

Additionally, an example git pre-commit hook is provided. To use this, place it in your project's `.git/hooks` folder as `pre-commit`.
