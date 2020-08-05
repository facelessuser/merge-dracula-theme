# Theme - Dracula

[Dracula](https://draculatheme.com/) theme for Sublime Merge 2. It is based off the Sublime Mariana color scheme, but
uses the classic Dracula color palette.

![Sublime Merge](./sublime_merge.png)

## Install

Git clone project or download into your Sublime Merge `Packages` folder as `Theme - Dracula`. Edit your merge
`Preferences.sublime-settings` file to use the Dracula theme:

```js
    "theme": "Dracula.sublime-settings"
```

## Dracula Pro?

Dracula Pro changed up the color palette a bit and added new variants such as Buffy, Van Helsing, and others. Dracula
Pro is also not free. Because of this, we only provide the "classic" Dracula palette.

We'd love to provide Pro variants, but while we think we have figured out the color palette for new Pro variants,
without the Pro color scheme being made public, we do not feel it would be proper to release our variants here.

For those who've acquired Pro through purchasing, the current color scheme can be customized with overrides to provide
Pro styles.

If at some future time, the Pro public scheme becomes available to the public, we will be happy to provide theme
variants here as well.

## Customize

The Dracula Pro Merge theme dynamically sources it's colors from the color scheme. While you are free to provide
overrides to the theme, it would normally be recommended to apply overrides to the color scheme if all you want is to
tweak the palette. Overriding the color scheme is all we will be covering at this time.

Customizing the color scheme can be useful if you'd like to things like tweak the background to be darker, or tweak
accents or even to update the palette for something like Dracula Pro variants, or even your own custom palette.

The color scheme provides a number of variables for the purpose of overrides.


This color scheme is designed in such a way as to be customizable. Simply override the background with the color of your
choice, and create comments and selections that adapt based on your background selection (or other color if you choose).
You can create an override file using the name `Dracula.sublime-color-scheme` in your `User` folder.

Want a pinkish theme? Plug in a pink hued background and tweak a couple variables. We will talk about them in sections:

1.  The base palette colors are the base Dracula colors. When creating a Dracula theme, these are the least likely to
    require overriding or it would no longer be a Dracula theme. This defines all the foreground colors. If you, for
    instance, knew the Pro palettes, you would most likely these with the new Pro palette, which would be the same
    across all variants.

    ```js
    // Static palette colors. These are constant through all variations.
    "foreground": "hsl(60, 30%, 96%)", // #f8f8f2
    "red": "hsl(0, 100%, 67%)",        // #ff5555
    "orange": "hsl(31, 100%, 71%)",    // #ffb86c
    "yellow": "hsl(65, 92%, 76%)",     // #f1fa8c
    "green": "hsl(135, 94%, 65%)",     // #50fa7b
    "cyan": "hsl(191, 97%, 77%)",      // #8be9fd
    "blue": "hsl(225, 27%, 51%)",      // #6272a4
    "pink": "hsl(326, 100%, 74%)",     // #ff79c6
    "purple": "hsl(265, 89%, 78%)",    // #bd93f9
    ```

    Dracula doesn't really define a "blue" per se, but here "blue" represents the classic palette's blue-ish comments.

1.  The next section provides a number of colors that it is expected users would alter for color scheme variants. This
    defines colors such as comments, backgrounds, alternate backgrounds (Markdown code blocks etc.), line highlights,
    selections, etc.

    ```
    // Variant specific colors (change these for variants)
    "background": "hsl(231, 15%, 18%)", // #282a36
    "selection": "hsl(232, 14%, 31%)",  // #44475a
    "comment": "var(blue)",             // #6272a4
    "line-highlight": "var(selection)",
    "alt-background": "color(var(background) l(+ 4%))",
    "accent": "var(blue)",
    ```

    If attempting a Pro style variant, you might change the `background`. You might derive `comment` from one of the
    core colors and adjust saturation and lightness. You might derive a new `selection` from your new `background`. You
    may also want a different accent.

1. The last group of are areas that are less likely to require modification, though you may want to make the caret
   jump out more by setting it to `pink`, or maybe you wish to alter the `highlight` of find results.

   ```js
    // UI elements derived from color schemes
    "caret": "var(foreground)",
    "block-caret": "var(caret)",
    "highlight": "var(yellow)",
    "shadow": "hsl(0, 0%, 0%)",
    "stack": "color(var(comment) s(100%) l(75%))",
    "darken": "hsl(0, 0%, 13%)",
    ```

For an example, let's say we wanted to create our own unofficial Van Helsing variant. Dracula Pro provides a darker
variant called Van Helsing. We will not give the actual Van Helsing palette, but simply show how to make one with the
"classic" palette.

-   We will take the existing `blue` that we use for comments and darken it and adjust the saturation considerably.
-   We will derive a selection from that is similar to the background but lighter.
-   We will derive a comment that also matches the background, but stands out.
-   We will derive a line highlight from the background as well, though you could just use `selection` as a suitable
    line highlight as well.
-   Our `alt-background` will be require us to lighten it more than we do in the "classic" colorscheme as we need more
    contrast on such a dark background.
-   Lastly, we will continue to use the accent, but you are free to change this to anything.

```js
// Variant specific colors (change these for variants)
"background": "color(var(blue) s(15%) l(5%))",
"selection": "color(var(background) s(15%) l(30%))",
"comment": "color(var(blue) s(25%) l(55%))",
"line-highlight": "color(var(background) s(25%) l(25%))",
"alt-background": "color(var(background) l(+ 6%))",
"accent": "var(blue)",
```

Here we get something similar to Van Helsing, but with a classic palette.

![Darker](./sublime_merge_darker.png)

We could just as easily change the colors and produce a Buffy like variant as well:

![Pink](./sublime_merge_pink.png)

## Notes

We include the color scheme here for convenience and for the off chance that the user uses only Sublime Merge and not
Sublime Text.

We do not actually have to include the color scheme in this package if you were using the color scheme in Sublime Text.
Merge looks for color schemes (`.sublime-color-scheme`) in Sublime Text installs and uses those in Merge. Assuming they
contain the required Merge specific rules, they should work fine. So if you were using the color scheme in this package
already in Sublime Text, Merge would find it and use it making the inclusion here unnecessary.
