# Font Setup Instructions

This document provides instructions for setting up the custom fonts for your Jekyll website.

## Font Files

Place the following font files in the `assets/fonts/` directory:

### Inter Thai Web Loopless (for headings)
- `InterSansTHLoopless.woff2`
- `InterSansTHLoopless.woff`
- `InterSansTHLoopless-Bold.woff2`
- `InterSansTHLoopless-Bold.woff`
- `InterSansTHLoopless-Italic.woff2`
- `InterSansTHLoopless-Italic.woff`
- `InterSansTHLoopless-BoldItalic.woff2`
- `InterSansTHLoopless-BoldItalic.woff`

### Inter Thai Web Looped (for body text)
- `InterSansTHLooped.woff2`
- `InterSansTHLooped.woff`
- `InterSansTHLooped-Bold.woff2`
- `InterSansTHLooped-Bold.woff`
- `InterSansTHLooped-Italic.woff2`
- `InterSansTHLooped-Italic.woff`
- `InterSansTHLooped-BoldItalic.woff2`
- `InterSansTHLooped-BoldItalic.woff`

## Important: Fix the main.scss Front Matter

The `assets/css/main.scss` file requires proper Jekyll front matter. Please ensure it has the following format:

```scss
---
# Only the main Sass file needs front matter (the dashes are enough)
---

/* Import custom font declarations */
@import "custom/fonts";

/* Import custom variables */
@import "custom/variables";

/* Import the minimal-mistakes theme */
@import "minimal-mistakes";

/* Import custom styles */
@import "custom/custom";

/* Custom styles to override theme defaults */
.sidebar.sticky {
    opacity: 1 !important;
    /* Force opacity to 1 at all times, overriding any default or hover states */
}
```

**Note:** The triple dashes `---` must be on their own lines at the beginning and end of the front matter.

## Testing Your Setup

After placing the font files in the correct directory and fixing the front matter, you can test your setup by running:

```bash
bundle exec jekyll serve
```

This will start a local server where you can view your site with the custom fonts applied.

## What Has Been Set Up

1. **Font Files Directory**: `assets/fonts/` - Place your font files here
2. **Font Declarations**: `_sass/custom/_fonts.scss` - Contains @font-face declarations
3. **Font Variables**: `_sass/custom/_variables.scss` - Overrides theme font variables
4. **Custom Styles**: `_sass/custom/_custom.scss` - Additional styling for specific elements
5. **Main Stylesheet**: `assets/css/main.scss` - Imports all the custom files

## Implementation Details

- Headings (h1, h2, h3, etc.) will use "Inter Thai Web Loopless"
- Body text and other elements will use "Inter Thai Web Looped"
- The font declarations include normal, bold, italic, and bold-italic variants
