all: {{cookiecutter.project_name}}.pdf
{% if cookiecutter.template == "Simple Essay" %}
LATEX_FLAGS=-xelatex
{% else %}
LATEX_FLAGS=
{% endif %}
{{cookiecutter.project_name}}.pdf: {{cookiecutter.project_name}}.tex
	latexmk ${LATEX_FLAGS} {{cookiecutter.project_name}}.tex -pdf
continuous:
	latexmk ${LATEX_FLAGS} {{cookiecutter.project_name}}.tex -pvc -pdf -r ./latexmkrc
clean:
	latexmk -c
