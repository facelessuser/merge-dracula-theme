# Theme - Dracula

[Dracula](https://draculatheme.com/) theme for Sublime Merge 2.

Requires related [color scheme](https://github.com/facelessuser/sublime-dracula-scheme). The color scheme is based off
the Sublime Mariana color scheme, but uses the classic Dracula color palette. We do not use the official Dracula color
scheme as we feel ours, which uses the newer color scheme format, provides better scoping with Sublime Text 4 and
Sublime Merge 2. Our theme also expects certain variables that are only provided in our specific implementation of the
Dracula color scheme.

![Sublime Merge](screenshots/Merge%20-%20Dracula.png)

## Install

Assuming the required color scheme is installed, git clone the project or download it into your Sublime Merge `Packages`
folder as `Theme - Dracula`. Edit your merge `Preferences.sublime-settings` file to use the Dracula theme:

```js
    "theme": "Dracula.sublime-theme"
```

## Alternative Theme: Alucard

We also provide an additional theme called `Dracula (Alucard)`. Instead of of using the `Dracula.sublime-color-scheme`
provided by our [color scheme package](https://github.com/facelessuser/sublime-dracula-scheme), it uses the
`Dracula (Alucard).sublime-color-scheme` provided by the same package. The Alucard color scheme deviates from Dracula
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

While we feel we have been able to reverse engineer the Pro color palette close enough, and do have Pro variants of the Dracula color scheme on a private repository, we are uncertain if we can legally release our Pro variant color schemes. Without these Pro variants of the color scheme, the Pro Merge themes are currently unusable by the general public. The
Pro Merge themes do not provide the Dracula palettes themselves as they rely on the color scheme to provide the colors,
so they do not violate any licensing. So they are included, but require a valid color scheme to be functional.

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

If you wish to create your own Pro color schemes, you can follow the guide [here](https://github.com/facelessuser/sublime-dracula-scheme#how-to-create-pro-variants).
