# Theme - Dracula

[Dracula](https://draculatheme.com/) theme for Sublime Merge 2.

Requires related [color scheme](https://github.com/facelessuser/sublime-dracula-scheme). The color scheme is based off
the Sublime Mariana color scheme, but uses the classic Dracula color palette. We do not use the official Dracula color
scheme as we feel ours, which uses the newer color scheme format, provides better scoping with Sublime Text 4 and
Sublime Merge 2. Our theme also expects certain variables that are only provided in our specific implementation of the
Dracula color scheme.

![Sublime Merge](screenshots/Merge%20-%20Dracula.png)

## Install

Assuming the required color scheme is installed, git clone project or download into your Sublime Merge `Packages`
folder as `Theme - Dracula`. Edit your merge `Preferences.sublime-settings` file to use the Dracula theme:

```js
    "theme": "Dracula.sublime-theme"
```

## Alternative Theme: Alucard

We also provide an additional theme called `Dracula (Alucard)`. Instead of of using the `Dracula.sublime-color-scheme`
provided by our [color scheme package](https://github.com/facelessuser/sublime-dracula-scheme), it uses the
`Dracula (Alucard).sublime-color-scheme` provided by that same package. The Alucard color scheme deviates from Dracula
"proper" by making some minor adjustments to the color palette. Mainly, it uses different colors for line highlight.

In the past, some people have complained about Dracula's default line highlight. Claims have been made that it can make
some text difficult to see. If you have line highlighting enabled in Merge, and feel the default line highlighting is
troublesome, Alucard may be a better option.

Alucard uses a line highlight color that looks more subtle against the background and makes text easier to see. In all
other respects, the theme looks exactly like the default Dracula theme. So if line highlight is not enabled in Merge,
or you are a Dracula purist, then the classic theme may be the preferred option.

```js
    "theme": "Dracula (Alucard).sublime-theme"
```

## Dracula Pro?

Do we support Dracula Pro? Yes and no. In short, yes we provide the themes, but they will not work for the general
public as the required Pro color schemes are currently private. We do not want our repository taken down and are unsure
if we can make the variant color schemes public without repercussions.

Dracula Pro changed up the color palette a bit and added new variants such as Buffy, Van Helsing, and others. The
official Dracula Pro theme is also not free.

While we feel we have reversed engineered the color palette, and do have Pro variants of the Dracula color scheme on a
private repository, we are uncertain if we can legally release our Pro variant color schemes. Without these Pro variants
of the color scheme, the Pro Merge theme variants are currently unusable by the general public. The Pro Merge themes
do not provide the Dracula palettes themselves as they rely on the color scheme to provide the colors, so they do not
violate any licensing. So they are included, but require a valid color scheme to be functional.

For those who've acquired the official Dracula Pro theme (which we are **not** affiliated with) through purchasing, the
current, public Dracula color scheme that we provide can be altered with the official Dracula Pro palette. As long as
Merge can find the color schemes with the name expected by the specific Dracula Pro Merge theme, things should work just
fine.

The Alucard color scheme is the best base to use if attempting to create a Pro color scheme from the public Dracula
color schemes as it treats line highlights in a way that better represents what the Pro color schemes do.

If at some future time, the Pro public scheme becomes available to the public, or we feel we can safely release them
without repercussions, we will be happy to make our Pro color scheme variants public allowing the use of the Merge Pro
variants without any manual workarounds.

Assuming a proper color scheme is provided, these are what the available Pro themes look like. Alucard is an unofficial
theme which provides a classic look, but uses the newer Pro palette.

Dracula Pro:

![Pro](screenshots/Merge%20-%20Pro.png)

Dracula Pro (Alucard)

![Alucard](screenshots/Merge%20-%20Alucard.png)

Dracula Pro (Buffy)

![Buffy](screenshots/Merge%20-%20Buffy.png)

Dracula Pro (Blade)

![Blade](screenshots/Merge%20-%20Blade.png)

Dracula Pro (Lincoln)

![Lincoln](screenshots/Merge%20-%20Lincoln.png)

Dracula Pro (Morbius)

![Morbius](screenshots/Merge%20-%20Morbius.png)

Dracula Pro (Van Helsing)

![Van Helsing](screenshots/Merge%20-%20Van%20Helsing.png)

## How to Create Pro Variants?

Assuming you have access to the official Pro variant colors, Merge requires the following color schemes to be found:

- Pro: `Dracula Pro.sublime-color-scheme`
- Buffy: `Dracula Pro (Buffy).sublime-color-scheme`
- Blade: `Dracula Pro (Blade).sublime-color-scheme`
- Lincoln: `Dracula Pro (Lincoln).sublime-color-scheme`
- Morbius: `Dracula Pro (Morbius).sublime-color-scheme`
- Van Helsing: `Dracula Pro (Van Helsing).sublime-color-scheme`

Using the `Dracula (Alucard).sublime-color-scheme` as a base (found [here](https://github.com/facelessuser/sublime-dracula-scheme/blob/master/Dracula%20(Alucard)),
simply change the palette colors below to the appropriate colors. The official Dracula color scheme doesn't really
specify a `blue` color, and in the classic color scheme, we specified the comment color as the `blue`, but in the Pro
color schemes, it is defined as a color with the dominant hue as used in the Van Helsing variant (background hue) but
lightened and saturated to match the other primary colors. `blue` is not really a primary color in the Dracula palette,
but is used as an accent color for Van Helsing and Alucard and as an additional branch color in Merge etc.

```js
        // Static palette colors. These are constant through all variations.
        "foreground": "hsl(60, 30%, 96%)", // #f8f8f2
        "red": "hsl(0, 100%, 67%)",        // #ff5555
        "orange": "hsl(31, 100%, 71%)",    // #ffb86c
        "yellow": "hsl(65, 92%, 76%)",     // #f1fa8c
        "green": "hsl(135, 94%, 65%)",     // #50fa7b
        "cyan": "hsl(191, 97%, 77%)",      // #8be9fd
        "blue": "hsl(225, 100%, 75%)",     // #809fff
        "pink": "hsl(326, 100%, 74%)",     // #ff79c6
        "purple": "hsl(265, 89%, 78%)",    // #bd93f9
```

Then, simply change the "Variant Specific" as shown below. The dominant color for the Pro variant should be used in any
place noted as `var(dominant-color)`. For instance, if you were creating the Blade variant, you'd change 
`var(dominant-color)` to `var(cyan)`. Additionally, we've left `background` blank. Simply insert the appropriate
`background` color for the given Pro variant.

```js
        // Variant specific colors (change these for variants)
        "background": "",
        "selection": "color(var(background) s(15%) l(30%))",
        "comment": "color(var(dominant-color) s(25%) l(55%))",
        "line-highlight": "color(var(background) s(25%) l(25%))",
        "accent": "var(dominant-color)",
```

The dominant colors for the given Pro variant are found listed below:

- Pro: `purple`
- Buffy: `pink`
- Blade: `cyan`
- Lincoln: `yellow`
- Morbius: `red`
- Van Helsing: `blue`

Alucard is a little different from the other Pro variants and simply uses the following in the Pro variant. It uses
`blue` as its accent color, but we manually specify classic `comment` color and `background`.

```js
        // Variant specific colors (change these for variants)
        "background": "hsl(231, 15%, 18%)",
        "selection": "color(var(background) s(15%) l(30%))",
        "comment": "hsl(225, 27%, 51%)",
        "line-highlight": "color(var(background) s(25%) l(25%))",
        "accent": "var(blue)",
```
