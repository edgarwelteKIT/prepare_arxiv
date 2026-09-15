# prepare_arxiv

Prepare a LaTeX project for arXiv submission.

What it does:
  1. Compiles the original project with -recorder to determine which local
     files are actually used.
  2. Creates a NEW output directory containing only those required files.
  3. Flattens all required files into that directory.
  4. Rewrites common LaTeX references to use flattened filenames.
  5. Removes comments from all .tex files.
  6. Does not copy hidden files/directories or common LaTeX build artifacts.
  7. Appends the requested arXiv four-pass trigger after \\end{document}.

The original project is not modified.

Usage:
    
    python3 prepare_arxiv.py /path/to/project

or:

    python3 prepare_arxiv.py /path/to/project \
        --main paper.tex \
        --output /path/to/arxiv_submission

Requirements:
    pdflatex

Optional but recommended:
    latexmk
