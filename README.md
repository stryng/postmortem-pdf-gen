# PostMortem PDF Auto Generation Report
## Requirements Definitions
### OS - UBUNTU 18.xx - LTS
#### Requirements Definitions (R{x})
#### R1 - PDFLatex + Fonts - Maintained @ - https://gist.github.com/rain1024/98dd5e2c6c8c28f9ea9d
`sudo apt install texlive-latex-base texlive-fonts-recommended texlive-fonts-extra`

#### R2 - Pandoc
`sudo apt install pandoc`

#### PostMortem Template
Location - ./template/postmortem.md

#### PDF Generation Process
`pandoc --toc --standalone --smart --normalize template/postmortem.md --from markdown -t latex -s --output $(basename "$PWD").pdf`

#### PDF is generated on /postmortem-pdf-gen root as postmortem-pdf-gen.pdf file
`postmortem-pdf-gen# file postmortem-pdf-gen.pdf
postmortem-pdf-gen.pdf: PDF document, version 1.5`

Enjoy
