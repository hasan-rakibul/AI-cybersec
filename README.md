# ICT607 &ndash; Artificial Intelligence for Cybersecurity

## Helpful resources
## Blogs/tutorial
- [10 minutes to Pandas](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)

## Books
- [Dive into Deep Learning](https://d2l.ai/index.html)
- [Interpretable Machine Learning](https://christophm.github.io/interpretable-ml-book/)
- [Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/)

## Generating lab manuals from ipynb files
- Requirements
    ```
    sudo apt-get install pandoc
    sudo apt-get install texlive-xetex texlive-fonts-recommended texlive-plain-generic
    python -m pip install nbconvert
    ```
- `jupyter nbconvert --to latex <filename.ipynb> --output ICT607-lab-<number>-manual.tex`
- Change the `tex` file (what you like to have). For example, before `\begin{document}`around line 388 you can add/modify:
    ```
    \usepackage{fancyhdr,lastpage}
    \pagestyle{fancyplain}
    \fancyhf{}
    \renewcommand{\headrulewidth}{0pt}
    \rhead{\includegraphics[width=4cm]{../MU_wordmark_2021_red_RGB.png}}
    \fancyfoot[C]{\footnotesize\textbf{\thepage} of \pageref*{LastPage}}
    \title{ICT607: Artificial Intelligence for Cybersecurity}
    \date{Experiment <number>}
    ```
- `xelatex' <manual filename.tex>`
- `rm *.log *.aux *.out` to remove unnecessary files
- Alternatively, run `colab_ipynb_to_pdf.ipynb` to generate pdf from Google colab directly (have less control such as always having today's date on the top sheet)