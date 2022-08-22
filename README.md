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

• [Ayu Mirage Plus](https://github.com/whosydd/ayu-mirage-plus) (dark)

Vivid colours, even luminance. Distinct semantic highlighting.

• [Noctis - by Liviu Schera](https://marketplace.visualstudio.com/items?itemName=liviuschera.noctis) (light and dark)

Vibrant colours, even luminance. Distinct semantic highlighting. Many great variations. [Extra luminance sometimes used for semantic highlighting.]

• [After Dark - by Simeon Kerkola](https://marketplace.visualstudio.com/items?itemName=ssmi.after-dark&ssr=false#review-details) (dark+)

Vivid colours, even luminance. Distinct semantic highlighting. [no colour for data constructors]

• [Atom One Dark Coal - by shiftybody](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight#common_weight_name_mapping) (dark)

Soft colours, even luminance. Distinct semantic highlighting. [no colour for operators]

• [Monokai Pro - by Monokai original author](https://marketplace.visualstudio.com/items?itemName=monokai.theme-monokai-pro-vscode) (dark)

Very popular. Icon theme + Colour theme. Icon themes are nice (better than the bulit-in), can be applied separately from the colour theme. Some shortcomings on its colour theme: does not distinguish module names by unique colour; like 99% of themes on the marketplace, comments are too muted thus hard to read; free trial with occasional nag to pay. [no colour for data constructors]

• [Vim Theme - by HarryHopkinson](https://marketplace.visualstudio.com/items?itemName=HarryHopkinson.vim-theme) (dark; has light theme too but not good)

Coherent colours avoiding blue shades. Distinct semantic highlighting. Choice of contrast level (soft, medium, hard).

### built-in/pre-installed themes (the good ones)

Solarized {Light,Dark} | Tomorrow Night Blue (dark)

These are fine, with some quirks. Solarized's colour for control flow keywords is too muted. Tomorrow Night Blue has very bright font; [no colour for data constructors].

### customizing a colour theme

https://code.visualstudio.com/docs/getstarted/themes#_customizing-a-color-theme

Many themes have comments that are too dark. Use this to customize comments colour for each theme:

```json
"editor.tokenColorCustomizations": {
    "[Ayu Mirage Plus]": {
        "comments": "#999"
    },
    "[Monokai Pro]": {
      "comments": "#999"
    }   
},
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
  "vim.searchMatchColor": "hsl(0,0%,30%)",
  "vim.searchMatchTextColor": "rgba(120,255,255,0.9)",
  "vim.searchHighlightColor": "rgba(120,255,255,0.9)",
  "vim.searchHighlightTextColor": "hsl(0,0%,30%)",
  "vim.textwidth": 79,
```

• utilities
: [Font Switcher](https://marketplace.visualstudio.com/items?itemName=evan-buss.font-switcher)
| [Bookmarks](https://marketplace.visualstudio.com/items?itemName=alefragnani.Bookmarks)
| [Rainbow Highlighter](https://marketplace.visualstudio.com/items?itemName=cobaltblu27.rainbow-highlighter)
| [Tab out of quotes, brackets, etc](https://marketplace.visualstudio.com/items?itemName=albert.TabOut)
| [Draw.io Integration](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio)
