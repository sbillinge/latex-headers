# latex_headers
A repo for keeping our shared latex headers

1. under the `\\documentclass` line in your latex file type
2. `\\input{|"curl --stderr /dev/null https://raw.githubusercontent.com/Billingegroup/latex-headers/main/latex_headers/<header_name>.tex"}` for each file you want to include. Recommended at the time of writing is `cmds_general.tex`, `cmds_programs.tex` and `packages.tex`
3. or `\\input{"wget -O - https://raw.githubusercontent.com/Billingegroup/latex-headers/main/latex_headers/packages.tex"}` (note, this command has not been tested, please fix if it needs to be updated)
4. when you compile the latex add `--shell-escape` to your latex command. e.g.,
5. `latex --shell-escape <filename>.tex` or
6. `pdflatex --shell-escape <filename>.tex`

Crib: copy-paste this into your file below the documentclass line:

```
\input{|"curl --stderr /dev/null https://raw.githubusercontent.com/Billingegroup/latex-headers/main/latex_headers/cmds_general.tex"} \input{|"curl --stderr /dev/null https://raw.githubusercontent.com/Billingegroup/latex-headers/main/latex_headers/cmds_programs.tex"} \input{|"curl --stderr /dev/null https://raw.githubusercontent.com/Billingegroup/latex-headers/main/latex_headers/packages.tex"} %
% to compile, use
% pdflatex --shell-escape <filename>.tex
```

Please see Simon's group meeting talk [here](https://gitlab.thebillingegroup.com/talks/2212sb_grpmtg/-/blob/main/manuscripts_and_figures.pptx) for more details.

Group matplotlib style-files are held in the [billingegroup/bg-mpl-stylesheets](https://github.com/Billingegroup/bg-mpl-stylesheets) repository. Instructions for using them can be found in the [Readme.md](https://github.com/Billingegroup/bg-mpl-stylesheets) in that repo, with some discussion in Simon's group meeting talk [here](https://gitlab.thebillingegroup.com/talks/2212sb_grpmtg/-/blob/main/manuscripts_and_figures.pptx)
