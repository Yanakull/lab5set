SRC = presentation.md
FILES = presentation.pdf presentation.html

%.pdf: %.md
	pandoc "$<" -t beamer --slide-level=2 --pdf-engine=xelatex \
   	  -V mainfont="DejaVu Serif" \
   	  -V sansfont="DejaVu Sans" \
   	  -V monofont="DejaVu Sans Mono" \
   	  -V fontenc=T2A \
   	  -V lang=russian \
          -o "$@"

%.html: %.md
	pandoc "$<" --embed-resources --standalone -t revealjs -V theme=beige -o "$@"

all: $(FILES)
	@echo " PDF и HTML версии созданы успешно!"
	@echo " PDF: presentation.pdf"
	@echo " HTML: presentation.html"

clean:
	rm -f $(FILES)
	@echo " Очистка завершена"

.PHONY: all clean
