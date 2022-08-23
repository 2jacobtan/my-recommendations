# Fonts (all with ligature support)

### • JetBrains Mono: [main site](https://www.jetbrains.com/lp/mono/) | [github release](https://github.com/JetBrains/JetBrainsMono/)

Pragmatic, no-frills, elegant design optimised for easy/fast reading.
Unique feature: rectangular characters allow eyes to smoothly scan through text.

### • Like JetBrains Mono, but with more "character" (less strictly rectangular character designs)
  [**Fira Code**](https://github.com/tonsky/FiraCode)
| [**Cascadia Code**](https://github.com/microsoft/cascadia-code)
| [**Hasklig** (variant of Source Code Pro with added ligatures)](https://github.com/i-tu/Hasklig)

### • Victor Mono (narrow; cursive italics) | [github release](https://github.com/rubjo/victor-mono)

## font weight

In text editor, tweak font weight setting for optimum clarity on computer screen.

extra reference https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight#common_weight_name_mapping

# VSCode

## themes

### S-tier (personal favourites)

• [Ayu - by teabyii](https://marketplace.visualstudio.com/items?itemName=teabyii.ayu) (dark; has light theme too but not good)

Vivid colours, even luminance. Distinct semantic highlighting. Includes variations with different contrast levels.

Icon theme + Colour theme. Icon theme is great (especially the "opened folder" icon! much better than the bulit-in), can be applied separately from the colour theme.

Forked variants: [Ayu Green](https://marketplace.visualstudio.com/items?itemName=Siris01.ayu-green) | [Ayu Baby Blue](https://marketplace.visualstudio.com/items?itemName=KF.ayu-baby-blue) | [Ayu Mirage Plus](https://marketplace.visualstudio.com/items?itemName=GY.ayu-mirage-plus)

• [Moonlight II - by atomiks](https://marketplace.visualstudio.com/items?itemName=atomiks.moonlight) (dark)

Vivid colours, even luminance. Distinct semantic highlighting. Optional italics. Medium contrast.

Similar feel to Ayu, but with blue and orange switched.

Incredible semantic highlight colour variety (e.g. JSON has different colours for deeper nesting).

• [Vim Theme - by HarryHopkinson](https://marketplace.visualstudio.com/items?itemName=HarryHopkinson.vim-theme) (dark; light theme A-tier)

Coherent colours avoiding blue shades. Distinct semantic highlighting. Choice of contrast level (soft, medium, hard).

Feels like Moonlight II, but with an orange-red filter.

• [After Dark - by Simeon Kerkola](https://marketplace.visualstudio.com/items?itemName=ssmi.after-dark&ssr=false#review-details) (dark)

Vivid colours, even luminance. Distinct semantic highlighting. Medium contrast. [no colour preset for data constructors]

I consider this S-tier with the tweaks I've made (see `customizing a colour theme` section below).

### A-tier (great in their own right)

• [Noctis - by Liviu Schera](https://marketplace.visualstudio.com/items?itemName=liviuschera.noctis) (light and dark)

Vibrant colours, even luminance. Distinct semantic highlighting. Includes many colour variations. Very fancy.

### B-tier (solid options; no frills)

• [Atom One Dark Coal - by shiftybody](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight#common_weight_name_mapping) (dark)

Soft colours, even luminance. Distinct semantic highlighting. [no colour preset for operators, see `customizing a colour theme` section below]

A fork of [One Dark Pro - by binaryify](https://marketplace.visualstudio.com/items?itemName=zhuangtongfa.Material-theme), super popular theme.

• [Monokai Pro - by Monokai original author](https://marketplace.visualstudio.com/items?itemName=monokai.theme-monokai-pro-vscode) (dark)

Icon theme + Colour theme. Icon themes are nice (better than the bulit-in), can be applied separately from the colour theme.

Some shortcomings on its colour theme: does not distinguish module names by unique colour; like 90% of themes on the marketplace, comments are too muted thus hard to read; free trial with occasional nag to pay. [no colour preset for data constructors]

### built-in/pre-installed themes (the good ones)

• Solarized {Light,Dark}

Muted control flow keyword colours. "Boring," but it works.

• Tomorrow Night Blue (dark, high contrast)

Bright font; high contrast. [no colour preset for data constructors]

### customizing a colour theme

https://code.visualstudio.com/docs/getstarted/themes#_customizing-a-color-theme

Use this to customize each theme (lighten comments colour, add operator colour, etc.):

```json
    "[Ayu Mirage Plus]":{
      "editor.background": "#242936"
    },
    "[After Dark*]": {
      "editor.background": "#242936",
      "terminal.background": "#192430",
      "editorRuler.foreground": "#2f3646"
    }
  },
  "editor.tokenColorCustomizations": {
    "[Ayu Mirage Plus]": {
      "comments": "#789",
      "textMateRules": [
        { "scope":"keyword.operator",
          "settings": {
            "foreground": "#F29E74",
          }},
        { "scope":"keyword.other",
          "settings": {
            // "foreground": "#F29E74",
            "fontStyle": ""
          }}]
    },
    "[Ayu*]": {
      "textMateRules": [
        { "scope":"keyword.control",
          "settings": {
            // "foreground": "#e30",
            "fontStyle": "italic bold"
          }},
        { "scope":"entity.name",
          "settings": {
            "foreground": "#b9f",
            "fontStyle": "bold"
          }},
        // { "scope":"source",
        //   "settings": {
        //     "foreground": "#CBCCC6",
        //   }},
        { "scope":"storage.type",
          "settings": {
            // "foreground": "#95E6CB", // can't be changed
            "fontStyle": "italic"
          }},
        // { "scope":"constant.other",
        //   "settings": {
        //     "foreground": "#73D0FF",
        //   }}
        ]
    },
    "[Moonlight*]": {
      "textMateRules": [
        { "scope":"keyword.control",
          "settings": {
            // "foreground": "#bb5235",
            "fontStyle": "italic bold"
          }},
        { "scope":"keyword.other",
          "settings": {
            // "foreground": "#75afff"
            // "foreground": "#4af"
            // "foreground": "#65BCFF"
            // "foreground": "#C099FF" // original
          }},
        { "scope":"entity.name",
          "settings": {
            "fontStyle": "bold",
            "foreground": "#fb9de7"
          }}]
    },
    "[Noctis*]": {
      "textMateRules": [
        { "scope":"keyword.control",
          "settings": {
            // "foreground": "#e30",
            "fontStyle": "italic bold"
          }},
        { "scope":"keyword.operator",
          "settings": {
            "foreground": "#eb7",
            "fontStyle": ""
          }},
        { "scope":"storage.type",
          "settings": {
            // "foreground": "#eb7",
            "fontStyle": "italic"
          }}]
    },
    "[Monokai Pro]": {
      "comments": "#999"
    },
    "[*One Dark*]": {
      "textMateRules": [
        { "scope": "keyword.operator",
          "settings": {
            // "foreground": "#e40"
            // "foreground": "#f88"
            // "foreground": "#4c8"
            // "foreground": "#48f"
            "foreground": "#7cf"
            // "foreground": "#99f"
            // "foreground": "#faf"
          }}]
    },
    "[After Dark*]": {
      "comments": "#89a",
      "textMateRules": [
        { "scope":"keyword.other",
          "settings": {
            "foreground": "#5bf"
          }},
        { "scope":"keyword.operator",
          "settings": {
            "foreground": "#d9b",
          }},
        { "scope":"keyword.control",
          "settings": {
            "fontStyle": "italic bold",
            "foreground": "#d9b"
          }},
        { "scope":"constant.other",
          "settings": {
            "foreground": "#ea6",
          }},
        { "scope":"storage.type",
          "settings": {
            "foreground": "#ec7",
            "fontStyle": "italic"
        }},
        { "scope":"entity.name",
          "settings": {
            "fontStyle": "bold",
            "foreground": "#BA7BCC"
        }}]
    },
    "[After Dark No Italics]": {
      "textMateRules": [
        { "scope": "comment",
          "settings": {
            "fontStyle": ""
          }},
        { "scope":"storage.type",
          "settings": {
            "fontStyle": ""
          }}]
    }
  }
```
(add to `settings.json`)

## extensions

• [VSpaceCode](https://vspacecode.github.io/) - Spacemacs like keybindings for Visual Studio Code (+ Vim emulation)

my `settings.json` entries for the Vim extension:

```json
  "vim.camelCaseMotion.enable": true,
  "vim.easymotion": true,
  "vim.easymotionKeys": "aoeuidhtns,pyfgcrl;qjkxbmwvz",
  "vim.replaceWithRegister": true,
  "vim.sneak": true,
  "vim.sneakUseIgnorecaseAndSmartcase": true,
  "vim.handleKeys": {
    "<C-w>": false,
    "<C-a>": false,
    "<C-x>": false,
    "<C-j>": false,
    "<C-l>": false,
    "<C-c>": false,
    "<C-k>": false,
    "<C-[>": false,
    "<C-]>": false,
    // "<C-pageup>": false,
    // "<C-pagedown>": false,
  },
  
  "vim.visualstar": true,
  "vim.hlsearch": true,
  "vim.highlightedyank.enable": true,
  "vim.showMarksInGutter": true,
  "vim.searchMatchColor": "rgba(120,255,255,0.9)",
  "vim.searchMatchTextColor": "hsl(0,0%,30%)",
  "vim.searchHighlightColor": "hsl(0,0%,50%)",
  "vim.searchHighlightTextColor": "rgba(120,255,255,0.9)",
  "vim.textwidth": 79,
```

• utilities
: [Font Switcher](https://marketplace.visualstudio.com/items?itemName=evan-buss.font-switcher)
| [Bookmarks](https://marketplace.visualstudio.com/items?itemName=alefragnani.Bookmarks)
| [Rainbow Highlighter](https://marketplace.visualstudio.com/items?itemName=cobaltblu27.rainbow-highlighter)
| [Tab out of quotes, brackets, etc](https://marketplace.visualstudio.com/items?itemName=albert.TabOut)
| [Draw.io Integration](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio)
