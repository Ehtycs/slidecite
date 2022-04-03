# Slidecite
A dead simple way to present citation information in beamer slides. See [slidebib.pdf](slidebib.pdf) and it's souce code [slidebib.tex](slidebib.tex) for usage demonstration and the actual source code of the tool.

# Why
Sometimes you want to refer to some source in the middle of the slide and show the source in the bottom of the slide. Thebibliography is not capable to do this. One way to achieve this is to use footnotes, but their numbering is only relevant inside the slide in question.

You could probably use bibtex + biber citation management to achieve this somehow but in most use cases this is using a sledgehammer to kill a fly. It takes time and effort to set bibtex up including the .bib files and correct bibentry formats. Sometimes what you want is just a dead simple list of manually formatted bibentries without any fancyness which ''just works''.

# How
Take the ~40 lines of code and comments from [slidebib.tex](slidebib.tex) between the BEGIN and END lines and copy & paste it to your beamer presentation's preamble. Then add the bibentries and cites and to each slide you want them to be visible, and you are done. 

# How it works
It's just a glorified enumerate environment including a custom counter. Nothing fancy, no black magic. No extra packages needed. 

# Missing functionality
- Recall a bibentry from previous slides and show the entry also on current slide. (Citing entries from previous slides works.)
- Display a list of all references made thus far e.g. in the end of the presentation. 
