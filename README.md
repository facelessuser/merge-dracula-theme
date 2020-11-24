# Theme - Dracula

[Dracula](https://draculatheme.com/) theme for Sublime Merge 2. It is based off the Sublime Mariana color scheme, but
uses the classic Dracula color palette.

Requires related [color scheme](https://github.com/facelessuser/sublime-dracula-scheme).

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
"proper" by making some minor adjustments to the color palette. Mainly it uses different colors for line highlight which
doesn't actually look as good with the background and makes comments more difficult to read. If you don't mind a slight
deviation from Dracula "proper" you can use this theme:

```js
    "theme": "Dracula (Alucard).sublime-theme"
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

The theme changes dynamically based on the color scheme. In order to adjust the colors, simply override the color scheme
with your desired changes. See the color schemes [documentation](https://github.com/facelessuser/sublime-dracula-scheme).
