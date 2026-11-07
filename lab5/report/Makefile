all: report.pdf report.docx

report.pdf: temp_report.md
	pandoc temp_report.md -o report.pdf \
        --pdf-engine=xelatex \
        -V mainfont="Liberation Serif" \
        -V sansfont="Liberation Sans" \
        -V monofont="Liberation Mono" \
        -V geometry:margin=2.5cm \
        --number-sections
        --number-offset=0

report.docx: temp_report.md
	pandoc temp_report.md -o report.docx \
	--number-sections

clean:
	rm -f report.pdf report.docx

.PHONY: all clean
