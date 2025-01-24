# Theme - Dracula

[Dracula](https://draculatheme.com/) theme for Sublime Merge 2.

Requires related [color scheme](https://github.com/facelessuser/sublime-dracula-scheme). The color scheme is based off
the Sublime Mariana color scheme, but uses the classic Dracula color palette. We do not use the official Dracula color
scheme as we feel ours, which uses the newer color scheme format, provides better scoping with Sublime Text 4 and
Sublime Merge 2. Our theme also expects certain variables that are only provided in our specific implementation of the
Dracula color scheme. Additionally, we also provide Dracula Pro inspired variants in our color scheme package as well.

![Sublime Merge](screenshots/Merge%20-%20Dracula.png)

## Install

Assuming the required color scheme is installed, git clone the project or download it into your Sublime Merge `Packages`
folder as `Theme - Dracula`. Edit your merge `Preferences.sublime-settings` file to use the Dracula theme:

```jsonc
//  Packages/User/Preferences.sublime-settings

{
    "theme": "Dracula.sublime-merge-theme"
}
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

```jsonc
//  Packages/User/Preferences.sublime-settings

{
    "theme": "Dracula (Alucard).sublime-merge-theme"
}
```

## Dracula Pro

**We are not affiliated with Dracula Pro, nor do we condone using the official paid for themes without paying for them,
but this theme is an original work that uses the Dracula Pro palette, the theme itself is not derived from the source of
any official Dracula theme.**

Sublime Merge supports the Dracula Pro variants that are provided in our [Dracula color schemes](https://github.com/facelessuser/sublime-dracula-scheme).
The Sublime Merge theme pulls the colors directly from the color schemes. The Pro color schemes were derived via
inspection of the official [Dracula Pro site](https://draculatheme.com/pro). All the colors are found in the official
site, and any that were not were derived from the information gathered there.

For those who want access to officially supported Dracula themes, they should consider purchasing Dracula pro from the
official [Dracula Pro site](https://draculatheme.com/pro).

### Dracula Pro (Alucard)

The Dracula Pro (Alucard) theme is just like the Alucard theme except it uses the Pro palette and the classic Dracula
background and comments.

![Alucard](screenshots/Merge%20-%20Alucard.png)

### Dracula Pro

![Pro](screenshots/Merge%20-%20Pro.png)

### Dracula Pro (Alucard)

![Alucard](screenshots/Merge%20-%20Alucard.png)

### Dracula Pro (Buffy)

![Buffy](screenshots/Merge%20-%20Buffy.png)

### Dracula Pro (Blade)

![Blade](screenshots/Merge%20-%20Blade.png)

### Dracula Pro (Lincoln)

![Lincoln](screenshots/Merge%20-%20Lincoln.png)

### Dracula Pro (Morbius)

![Morbius](screenshots/Merge%20-%20Morbius.png)

### Dracula Pro (Van Helsing)

![Van Helsing](screenshots/Merge%20-%20Van%20Helsing.png)
