# WEHI/UniMelb LaTeX Thesis Template

A comprehensive LaTeX template for Honours, Masters, and PhD theses, specifically tailored for submission to the Walter and Eliza Hall Institute of Medical Research (WEHI) and the University of Melbourne. This template is based on the Alcázar template by Juan Del Pino Mena, adapted to meet WEHI and University of Melbourne requirements.

![image](https://github.com/user-attachments/assets/c6f6ac9a-9311-417f-a614-fdcceafaf295)

## Features

- Pre-configured thesis structure following WEHI/UniMelb guidelines
- Customizable title page with WEHI and University of Melbourne branding
- Built-in citation and bibliography management
- Chapter and section templates
- Figure and table management
- Support for mathematical equations, scientific notation and formatted code snippets
- Customizable page layouts and formatting

## Prerequisites

To use this template, you'll need:
- A text editor or LaTeX IDE (Overleaf recommended)
- Basic familiarity with LaTeX syntax

## Using the Template in Overleaf

### Initial Setup

1. **Download the Template**
   - Go to the GitHub repository
   - Click the green "Code" button
   - Select "Download ZIP"

2. **Create New Overleaf Project**
   - Log into your Overleaf account
   - Click "New Project"
   - Select "Upload Project"
   - Drag and drop the downloaded ZIP file or click to browse
   - Wait for the upload to complete

### Project Configuration

1. **Compiler Settings**
   - Click on "Menu" in the top-left corner
   - Under "Compiler", select "pdfLaTeX"
   - Under "Main document", ensure `main.tex` is selected

2. **Recommended Project Settings**
   - Enable "Auto-compile" (Toggle in the top bar)
   - Set spell-check language as appropriate
   - Enable "Track Changes" if collaborating with supervisors

## File structure

The file structure of the template is simple and self-explanatory:

```
./
├── bibliography/               # BIBLIOGRAPHY
|   ├── bibliography.tex        # Bibliography generation
|   └── references.bib          # BibTeX references
|
├── figures/                    # Put your figures here
|
├── glossary/                   # GLOSSARY
|   ├── glossary.sty            # Glossary definitions
|   └── glossary.tex            # Glossary generation
|
├── opening/                    # OPENING
|   ├── resources/              # Graphics used in the opening (logos, etc)
|   |
|   ├── about.tex               # Details about the authors
|   ├── abstract.tex            # Abstract, in various languages
|   ├── acknowledgements.tex    # Acknowledgements
|   ├── dedication.tex          # Dedication
|   ├── opening.tex             # Structures the opening part of the document
|   └── publications.tex        # Your publications. Optional, comment line in opening.tex
|   └── titlepage.tex           # Title page
|
├── style/                      # STYLE
|   ├── alcazar.sty             # Style definition and configuration
|   ├── colors.sty              # Colors definition
|   └── pkgs.sty                # Only used to import packages
|
├── text/                       # TEXT
|   ├── appendix/               # Put your addendum here
|   |   ├── appendix.tex        # Appendix generation
|   |   └── thanks.tex          # Say thanks. Optional, comment line in main.tex
|   |
|   └── chapters/               # Put your chapters here
|
└── main.tex                    # The main document.
```

### Template Customization

1. **Personal Information**
   - In `main.tex` you will find some variable definitions, fill them in according to your thesis and the document will update all occurrences automatically. Update the following fields:
     - Thesis title
     - Your full name
     - Department/Lab information
     - Supervisor details
     - Submission date

2. **Declaration and Abstract**
   - Edit `opening/acknowledgements.tex` with your declaration
   - Update `opening/abstract.tex` with your abstract

3. **Chapter Management**
   - All chapter files are in the `chapters/` directory
   - Create new chapters by copying the existing chapter template

### Working with References

1. **Bibliography Setup**
   - Your references go in `bibliography/references.bib`
   - Use BibTeX format for all references
   - The template uses the numbered citation style by default (IEEE style)

2. **Adding Citations**
   - Use `\cite{key}` for standard citations. Ensure your reference is in `bibliography/references.bib`

### Figures and Tables

1. **Adding Figures**
   - Upload figures to the `figures/` directory
   - Use the provided figure templates in the example chapters
   - Recommended figure formats: PDF (vector), PNG (raster)

2. **Creating Tables**
   - Use the table templates provided in the example chapters
   - Consider using online table generators for complex tables
   - Remember to add table captions above the table

## Common Issues and Solutions

1. **Compilation Errors**
   - Clear cached files using "Clear Cache" in Overleaf menu
   - Check the log file for specific error messages
   - Ensure all referenced files are properly uploaded

2. **Figure Issues**
   - Verify figure paths are correct (case-sensitive)
   - Check figure formats are compatible
   - Ensure figures are actually uploaded to Overleaf

3. **Bibliography Problems**
   - Recompile project multiple times
   - Check for proper BibTeX formatting
   - Verify all cited references exist in `.bib` file

## Local Build Instructions

While this guide focuses on Overleaf usage, complete instructions for building the template locally are available in [in the original template by Juan Alcazar](https://github.com/dpmj/alcazar). If you prefer to work locally:

1. Visit the [original template's GitHub repository](https://github.com/dpmj/alcazar)
2. Refer to the main README.md file
3. Follow the "Local Installation" or "Building Locally" section

Local builds can offer advantages like:
- Faster compilation times
- Offline access
- Integration with local text editors
- Version control with Git
- Custom LaTeX package management

However, for most users, especially those new to LaTeX, Overleaf provides the easiest way to get started with this template.

## Getting Help

- For template issues: Create an issue on GitHub
- For Overleaf-specific problems: Consult [Overleaf Documentation](https://www.overleaf.com/learn)
- For WEHI/UniMelb specific questions: Contact your graduate research office
- For local build support: See the repository's documentation and README

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## Credits

- Original Alcázar template by Juan Del Pino Mena
- Adapted for WEHI/UniMelb by Mihin Perera


## Support

For template-specific issues, please open an issue on GitHub. For institution-specific questions:
- WEHI graduate research: [education@wehi.edu.au]
- University of Melbourne graduate research: [[contact details](https://research.unimelb.edu.au/contact)]
- For Overleaf-specific problems: Consult [Overleaf Documentation](https://www.overleaf.com/learn)

## Citation

If you use this template for your thesis, please consider acknowledging or citing it and the original template creator:

```bibtex
@misc{wehi-unimelb-thesis-template,
  author = {Perera, Mihin},
  title = {WEHI/UniMelb LaTeX Thesis Template},
  year = {2024},
  publisher = {GitHub},
  url = {https://github.com/[username]/wehi-unimelb-thesis-template}
}
@misc{alcazar-thesis-template,
  author = {Del Pino Mena, Juan},
  title = {Alcazar: A free and Open-Source LaTeX template for academic works},
  year = {2023},
  publisher = {GitHub},
  url = {https://github.com/dpmj/alcazar}
}
```


## License
    
This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/).

