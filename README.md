# Template LaTeX Project

A comprehensive LaTeX document for analysis and reporting.

## Features

- Mathematical equations and statistical analysis
- Tables and figures for data presentation
- Bibliography management
- Japanese font support

## Installation

### 1. Install MacTeX
```bash
brew install --cask mactex
```

### 2. Update TeX Live
```bash
sudo tlmgr update --self --all
sudo tlmgr paper a4
```

### 3. Copy LaTeX configuration
```bash
cp .latexmkrc ~/.
```

## Project Structure

```
report/
├── main.tex          # Main document file
├── egbib.bib         # Bibliography database
├── sec/
│   └── xxx.tex         # Section content
├── fig/              # Figures directory
├── tab/              # Tables directory
└── README.md         # This file
```

## Usage

### Compile the document
```bash
# Using pdflatex
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex

# Or using latexmk (recommended)
latexmk -pdf main.tex
```

### Clean auxiliary files
```bash
latexmk -c
```

## Document Sections

1. **Market Analysis and Methodology** - Data sources, KPIs, statistical analysis
2. **Executive Summary** - High-level findings and recommendations
3. **Market Overview** - Global economic indicators and asset class performance
4. **Risk Assessment** - Market risks and mitigation strategies
5. **Investment Recommendations** - Portfolio allocation and sector analysis
6. **Conclusion** - Summary and forward-looking recommendations

## Customization

### Colors
The document uses a professional color scheme:
- Primary Blue: RGB(0,114,178)
- Secondary Blue: RGB(86,180,233)
- Accent Orange: RGB(230,159,0)

### Adding Content
- Add new sections in the `sec/` directory
- Include figures in the `fig/` directory
- Add tables in the `tab/` directory
- Update bibliography in `egbib.bib`

## Dependencies

The document requires the following LaTeX packages:
- Core: graphicx, amsmath, geometry, url, cite
- Formatting: fancyhdr, multicol, float, color, xcolor
- Tables: booktabs, array, colortbl, tabularx
- Japanese: pxchfon
- Others: algorithm, algorithmic, bm, etc.

## Troubleshooting

### Common Issues
1. **Missing fonts**: Ensure Japanese fonts are installed
2. **Bibliography not showing**: Run `bibtex main` after pdflatex
3. **Table formatting**: Check for missing `\toprule`, `\midrule`, `\bottomrule`

### Getting Help
- Check LaTeX logs for error messages
- Ensure all required packages are installed
- Verify file paths and references

## License

This project is for educational and research purposes.
