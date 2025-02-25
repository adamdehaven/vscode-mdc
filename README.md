<img src="./images/icon.png" alt="MDC - Markdown Components by NuxtLabs" width="150" />

# MDC syntax highlight for Visual Studio Code

[![MDC Extension for VS Code][extension-version-src]][extension-href]
[![MDC Extension for VS Code][extension-downloads-src]][extension-href]
[![MDC Extension for VS Code][extension-installs-src]][extension-href]

Provides syntax highlighting and colon (`:`) matching for MDC (Markdown Components) files, as well as document folding and a format provider.

- [Download VS Code extension](https://marketplace.visualstudio.com/items?itemName=Nuxt.mdc)

Best used with:
- [Remark MDC](https://github.com/nuxtlabs/remark-mdc)
- [Markdown It MDC](https://github.com/antfu/markdown-it-mdc)

Or with Nuxt modules:
- [Nuxt MDC](https://github.com/nuxt-modules/mdc)
- [Nuxt Content](https://content.nuxt.com)

## Features

### Block Components

```md
::card
---
icon: IconNuxt
title: A complex card.
---

Default slot

#description
  ::alert
    Description slot
  ::
::
```

### Inline Components

```md
:button-link[A button link]{.text-bold}
<!-- or -->
:button-link{.text-bold}[A button link]
```

### Span Text

```md
Hello [World]!
```

### Attributes

```md
Hello [World]{.text-primary-500}!

[Link](#link){.text-primary-500 ref="noopener"}!

**Bold Text**{style="color: tomato"}

`Inline Code`{style="background: #333"}

_Italic Text_{#italic_text}
```

### Document folding

The extension enables document code folding for MDC block components (and nested components). Simply hover over the gutter of the line you'd like to fold and click on the icon to expand or collapse the range.

![code folding animation](images/code-folding.gif)

### Formatting

The plugin also enables a document format provider, disabled by default.

To globally configure document formatting in VS Code, search for `mdc.enableFormatting` in Settings.

Alternatively, to configure per-project, create or edit `.vscode/settings.json` in your project's root directory:

```jsonc
{
  // Required for the extension
  "mdc.enableFormatting": true,
  // Recommended (for `mdc` and `md`, depending on your usage)
  "[mdc]": {
    "editor.tabSize": 2,
    "editor.insertSpaces": true,
    "editor.detectIndentation": false,
    "editor.formatOnPaste": true
  }
}
```

> [!Note]
> Since the format provider utilizes spaces for indention, you may also need to configure your project to insert spaces for tabs within `.mdc` or `.md` files as recommended above.

### For more information

* [MDC Syntax Reference](https://content.nuxt.com/usage/markdown#introduction)


<!-- Badges -->
[extension-href]: https://marketplace.visualstudio.com/items?itemName=Nuxt.mdc
[extension-version-src]: https://img.shields.io/visual-studio-marketplace/v/Nuxt.mdc?label=Visual%20Studio%20Code&style=flat&colorA=020420&colorB=28CF8D
[extension-downloads-src]: https://img.shields.io/visual-studio-marketplace/d/Nuxt.mdc?style=flat&colorA=020420&colorB=28CF8D
[extension-installs-src]: https://img.shields.io/visual-studio-marketplace/i/Nuxt.mdc?style=flat&colorA=020420&colorB=28CF8D
