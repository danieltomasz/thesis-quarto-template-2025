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

## Alternative Fonts

If you don't have access to UGent Panno fonts, you can use Arial or another acceptable alternative by modifying the `include-in-header` section in `_quarto.yml`:

```yaml
# Comment out the UGent Panno font configuration and use a system font:
mainfont: "Arial"
```

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
