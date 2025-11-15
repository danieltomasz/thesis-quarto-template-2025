# UGent Panno Text Fonts

This directory should contain the official Ghent University Panno Text font files.

## Required Font Files

Place the following font files in this directory:

- `UGentPannoText-Normal.ttf`
- `UGentPannoText-SemiBold.ttf`

## Obtaining the Fonts

The UGent Panno font family is the official typeface of Ghent University. These fonts can be obtained from:

1. **UGent Staff Portal**: Available for UGent staff and PhD students through the university's internal resources
2. **UGent Style Guide**: Check https://styleguide.ugent.be/ for official font downloads
3. **Your Faculty**: Contact your faculty's communication department

## Font License

The UGent Panno fonts are proprietary and licensed for use by Ghent University members. Please ensure you have the proper authorization to use these fonts in your thesis.

## Automatic Fallback Fonts

**Good news!** If you don't have access to UGent Panno fonts, the template will automatically detect and use an appropriate fallback font. No configuration changes are needed!

The template checks for fonts in this order:
1. UGent Panno Text (if files are in this directory)
2. Arial (Windows/cross-platform)
3. Helvetica Neue (macOS)
4. Liberation Sans (Linux/open source, very similar to Arial)

Simply render your document and the template will use the best available option.

## Font Configuration

The fonts are configured in `_quarto.yml` with the following LaTeX commands:

```latex
\setmainfont[
  Path=include/fonts/,
  BoldFont=UGentPannoText-SemiBold.ttf,
  ItalicFont=UGentPannoText-Normal.ttf,
  BoldItalicFont=UGentPannoText-SemiBold.ttf,]
{UGentPannoText-Normal.ttf}
```

This configuration requires XeLaTeX or LuaLaTeX to compile.
