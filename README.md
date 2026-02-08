# Professional Resume Template

A clean, modern LaTeX resume template that outputs a professional one-page resume in PDF format.

## Preview

![Resume Preview](resume-preview.png)

## Features

- **Clean Design**: Professional, minimalist layout optimized for readability
- **One Page**: Compact format perfect for most applications
- **Easy to Customize**: Simple LaTeX structure with clear sections
- **FontAwesome Icons**: Social links and contact info with icons
- **Multiple Columns**: Efficient use of space for skills section
- **PDF Output**: High-quality PDF generation

## Requirements

- LaTeX distribution (TeX Live, MiKTeX, or MacTeX)
- `fontawesome5` package
- `geometry` package
- `hyperref` package

## Installation

### macOS
```bash
brew install --cask mactex
```

### Ubuntu/Debian
```bash
sudo apt-get update
sudo apt-get install texlive-full
```

### Windows
Download and install [MiKTeX](https://miktex.org/download) or [TeX Live](https://www.tug.org/texlive/)

## Quick Start

1. Clone this repository:
```bash
git clone https://github.com/username/ResumeTemplate.git
cd ResumeTemplate
```

2. Compile the resume:
```bash
make
```
or
```bash
pdflatex RESUME.tex
```

3. Edit `RESUME.tex` with your personal information
4. Recompile to generate your updated resume

## Customization

### Personal Information
Edit the heading section (lines 70-79) in `RESUME.tex`:
- Replace "Full Name Here" with your name
- Update contact information (phone, email, LinkedIn, GitHub, portfolio)
- Add or remove contact links as needed

### Sections
The template includes these standard sections:
- **Education**: Academic background and coursework
- **Experience**: Work history and internships  
- **Projects**: Personal and academic projects
- **Skills**: Technical skills and competencies

### Adding New Sections
Copy the pattern from existing sections:
```latex
\section{Section Name}
\resumeSubHeadingListStart
  % Add content here
\resumeSubHeadingListEnd
```

### Custom Commands
- `\resumeItem{}`: Single bullet point
- `\resumeSubheading{}`: Work/education entry with dates
- `\resumeProjectHeading{}`: Project entry with technologies

## Compilation Options

### Using Make (Recommended)
```bash
make          # Compile resume.pdf
make clean    # Remove auxiliary files
make view     # Compile and open PDF
```

### Manual Compilation
```bash
pdflatex RESUME.tex
# or for multiple passes (better references)
pdflatex RESUME.tex
pdflatex RESUME.tex
```

### Using XeLaTeX (alternative)
```bash
xelatex RESUME.tex
```

## File Structure

```
ResumeTemplate/
├── RESUME.tex          # Main resume file
├── Makefile           # Build automation
├── README.md          # This file
├── resume-preview.png # Preview image
└── .gitignore         # Git ignore file
```

## Tips

- **Keep it to one page**: This template is optimized for single-page resumes
- **Use action verbs**: Start bullet points with strong action verbs
- **Quantify achievements**: Include numbers and metrics when possible
- **Proofread**: Always check for spelling and grammar errors
- **Save as PDF**: Most employers prefer PDF format resumes

## Troubleshooting

### Missing Packages
If you encounter "Missing package" errors, install the required LaTeX packages:
```bash
tlmgr install fontawesome5 geometry hyperref
```

### Compilation Errors
- Ensure all LaTeX packages are installed
- Check for syntax errors in your edits
- Try compiling with `pdflatex -interaction=nonstopmode RESUME.tex` for detailed error output

### Font Issues
If FontAwesome icons don't appear, try:
```bash
tlmgr update fontawesome5
```

## License

This template is open source and available under the MIT License. Feel free to use, modify, and distribute for personal or commercial purposes.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request with improvements.

---

**Template created for easy customization and professional resume generation.**