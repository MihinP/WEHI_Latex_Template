# WEHI/UniMelb LaTeX Thesis Template

A comprehensive LaTeX template for Honours, Masters, and PhD theses, specifically tailored for submission to the Walter and Eliza Hall Institute of Medical Research (WEHI) and the University of Melbourne. This template is based on the Alcázar template by Juan Del Pino Mena, adapted to meet WEHI and University of Melbourne requirements.

## Features

- Pre-configured thesis structure following WEHI/UniMelb guidelines
- Customizable title page with WEHI and University of Melbourne branding
- Built-in citation and bibliography management
- Chapter and section templates
- Figure and table management
- Support for mathematical equations and scientific notation
- Customizable page layouts and formatting

## Prerequisites

To use this template, you'll need:
- A LaTeX distribution (TeX Live or MiKTeX recommended)
- A text editor or LaTeX IDE (VSCode, TeXmaker, or Overleaf recommended)
- Basic familiarity with LaTeX syntax

## Usage

1. Edit `main.tex` to customize your document structure
2. Add your chapters in the `chapters/` directory
3. Place your figures in the `figures/` directory
4. Update your bibliography in the `bibliography/` directory
5. Compile using your preferred LaTeX compiler

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## Credits

- Original Alcázar template by Juan Del Pino Mena
- Adapted for WEHI/UniMelb by Mihin Perera
- Contributors to the template (see [CONTRIBUTORS.md](CONTRIBUTORS.md))

## License

This project is licensed under the [MIT License](LICENSE.md) - see the LICENSE file for details.

## Support

For template-specific issues, please open an issue on GitHub. For institution-specific questions:
- WEHI graduate research: [education@wehi.edu.au]
- University of Melbourne graduate research: [[contact details](https://research.unimelb.edu.au/contact)]

## Citation

If you use this template for your thesis, please consider citing it:

```bibtex
@misc{wehi-unimelb-thesis-template,
  author = {Perera, Mihin},
  title = {WEHI/UniMelb LaTeX Thesis Template},
  year = {2024},
  publisher = {GitHub},
  url = {https://github.com/[username]/wehi-unimelb-thesis-template}
}
```


## Requirements

- `biber` for `biblatex`.
- `python 3` and `pygments` for the `minted` package.


## Build

### CLI, makefiles, etc.

This project can be easily built using the following commands with these recommended parameters. The `-shell-escape' flag is required for the `minted' package.

```bash
$ pdflatex -shell-escape -synctex=1 -interaction=nonstopmode -file-line-error main
$ biber main
$ makeglossaries main
$ pdflatex -shell-escape -synctex=1 -interaction=nonstopmode -file-line-error main
$ pdflatex -shell-escape -synctex=1 -interaction=nonstopmode -file-line-error main
```

### Overleaf

Works out of the box, no configuration required. Simply download this repo as a `.zip` and then upload the archive to Overleaf as a new project.

### LaTeX Workshop extension for VS Code / Codium

If you are using the LaTeX Workshop extension by James Yu, you need to add the following tools to your configuration file, under `latex-workshop.latex.tools` (In the UI, navigate to *Latex-workshop > Latex: Recipes > Edit in settings.json*): 

```json
{
    "name": "biber",
    "command": "biber",
    "args": [
        "%DOC%"
    ],
},
{
    "name": "makeglossaries",
    "command": "makeglossaries",
    "args": [
        "%DOCFILE%"
    ],
}
```

Edit the `pdflatex` entry as follows to include the `-shell-escape` argument, necessary for the `minted` package.

```json
{
    "name": "pdflatex",
    "command": "pdflatex",
    "args": [
        "-shell-escape",
        "-synctex=1",
        "-interaction=nonstopmode",
        "-file-line-error",
        "%DOC%"
    ],
    "env": {}
}
```

Now add a new recipe, under `latex-workshop.latex.recipes` (In the UI: *Latex-workshop > Latex: Tools > Edit in settings.json*):

```json
{
    "name": "alcazar",
    "tools": [
        "pdflatex",
        "makeglossaries",
        "biber",
        "pdflatex",
        "pdflatex"
    ]
}
```

And run the `alcazar' recipe on a `.tex' file from the project. 

**Note:** If you keep getting a `makeglossaries` error saying that `main.aux` could not be found, set the `latex-workshop.latex.autoBuild.cleanAndRetry.enabled` setting to `false` (in the UI, uncheck *"Latex-workshop > Latex > AutoBuild > Clean and retry: Enabled"*)


## File structure

The file structure of Alcázar is simple and self-explanatory:

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

- In `main.tex` you will find some variable definitions, fill them in according to your thesis and the document will update all occurrences automatically.
- Fill in your author information in the `opening/about.tex` file.


## License
    
This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/).


## Disclaimer

This work is not affiliated with any institution, and the references, logos, and the like are merely examples of usage. Any third-party resources included in this repository are the property of their respective owners, and are provided for convenience only.
