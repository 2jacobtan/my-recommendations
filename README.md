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

## Themes

Sorted by popularity https://marketplace.visualstudio.com/search?target=VSCode&category=Themes&sortBy=Installs

### vividly coloured

• [Ayu - by teabyii](https://marketplace.visualstudio.com/items?itemName=teabyii.ayu) (dark; light)

Choice of background brightness level (bordered, mirage, dark).

Includes icon theme that can be applied separately. "Opened folder" icon is very nice.

Family: [Ayu Green](https://marketplace.visualstudio.com/items?itemName=Siris01.ayu-green) | [Ayu Baby Blue](https://marketplace.visualstudio.com/items?itemName=KF.ayu-baby-blue) | [Ayu Mirage Plus](https://marketplace.visualstudio.com/items?itemName=GY.ayu-mirage-plus)

• [Moonlight II - by atomiks](https://marketplace.visualstudio.com/items?itemName=atomiks.moonlight) (dark)

Vast semantic highlight colour variety (e.g. JSON). Optional italics. Medium contrast.

Similar feel to Ayu, but with blue and orange switched.

• [After Dark - by Simeon Kerkola](https://marketplace.visualstudio.com/items?itemName=ssmi.after-dark&ssr=false#review-details) (deep dark)

Medium contrast, low brightness. [no colour preset for data constructors]

Needs some tweaks for colour variety. (see `customizing a colour theme` section below)

• [GitHub Theme - by GitHub](https://marketplace.visualstudio.com/items?itemName=GitHub.github-vscode-theme) (dark; light)

Choice of contrast levels (dimmed, default, high contrast). Loud orange-red colour used often.

### unique style

• [Vim Theme - by HarryHopkinson](https://marketplace.visualstudio.com/items?itemName=HarryHopkinson.vim-theme) (dark; light)

Warm colour temperature. Choice of contrast level (soft, medium, hard). [Is one amongst several Gruvbox clones.]

• [Noctis - by Liviu Schera](https://marketplace.visualstudio.com/items?itemName=liviuschera.noctis) (dark; light)

Fancy package with many colour filters.

### simple and elegant

• [Atom One Dark Theme - by Mahmoud Ali](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-theme-onedark) (dark)

Neutral, soft colours. Unassumingly easy on the eyes. [no colour preset for operators, see `customizing a colour theme` section below]

Family: [Atom One Dark Coal - by shiftybody](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight#common_weight_name_mapping) | [One Dark Pro - by binaryify](https://marketplace.visualstudio.com/items?itemName=zhuangtongfa.Material-theme) | [One Dark Vivid - by Kevin Kozee](https://marketplace.visualstudio.com/items?itemName=kkozee.theme-one-dark-vivid)

• [Night Owl - by sarah.drasner](https://marketplace.visualstudio.com/items?itemName=sdras.night-owl) (dark; light version less popular)

 Cool colour temerature. Dark theme is well-calibrated for low-light clarity (high contrast).

• [Monokai Pro - by Monokai original author](https://marketplace.visualstudio.com/items?itemName=monokai.theme-monokai-pro-vscode) (dark)

Pragmatic colour scheme. Normal shades of red, green, blue, orange clearly denote different elements.

Has several useful filters to tweak colour temperature and brightness.

Includes icon theme that can be applied separately.

Free trial with occasional nag to pay. [no colour preset for data constructors]

### built-in/pre-installed themes (the good ones)

• Solarized {Light,Dark}

Muted control flow keyword colours. "Boring," but it works.

• Tomorrow Night Blue (dark, high contrast)

Bright font, high contrast. [no colour preset for data constructors]

### customizing a colour theme

https://code.visualstudio.com/docs/getstarted/themes#_customizing-a-color-theme

Use this to customize each theme (lighten comments colour, add operator colour, etc.):

```jsonc
  "workbench.sideBar.location": "right",
  "workbench.colorCustomizations": {
    "editor.selectionBackground": "#aaa6",
    "editor.selectionHighlightBorder": "#808080",
    // "editor.hoverHighlightBackground": "#bbb3",
    "[Ayu Mirage Plus]":{
      "editor.background": "#242936"
    },
    "[*Dark*]": {
      "editorCursor.background": "#000",
      "editorCursor.foreground": "#fffc"
    }
    // "[After Dark*]": {
    //   "terminal.background": "#192430",
    //   "editor.background": "#242936",
    //   "editorRuler.foreground": "#2f3646",
    //   "editorIndentGuide.background": "#2f3646"
    // }
  },
  "editor.tokenColorCustomizations": {
    "[Ayu Mirage Plus]": {
      // "comments": "#789",
      "comments": "#B8CFE680",
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
    "[Vim*]": {
      "textMateRules": [
        { "scope":"keyword.control",
          "settings": {
            "fontStyle": "italic bold"
          }},
        { "scope":"storage.type",
          "settings": {
            "fontStyle": "italic"
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
            "foreground": "#d1b81a",
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
  },
  "terminal.integrated.cursorBlinking": true
}
```
(add to `settings.json`)

## extensions

• [VSpaceCode](https://vspacecode.github.io/) - Spacemacs like keybindings for Visual Studio Code (+ Vim emulation)

my `settings.json` entries for the Vim extension:

```jsonc
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
