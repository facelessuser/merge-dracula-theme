# merge-dracula-theme

[Dracula](https://draculatheme.com/) theme for Sublime Merge 2 (may or may not work on Sublime Merge 1).

![Sublime Merge](./sublime_merge.png)

## Install

Git clone project or download into your Sublime Merge `Packages` folder. Edit your merge `Preferences.sublime-settings`
file to use the Dracula theme:

```js
    "theme": "Dracula.sublime-settings"
```

## Notes

We do not actually have to include the color scheme in this package if you were using the color scheme in Sublime Text.
Merge looks for color schemes (`.sublime-color-scheme`) in Sublime Text installs and uses those in Merge. Assuming they
contain the required Merge specific rules, they should work fine. So if you were using the color scheme in this package
already in Sublime Text, Merge would find it and use it making the inclusion here unnecessary, but it is included here
as a convenience.
