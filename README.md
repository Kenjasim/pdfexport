# pdfexport
A simple bash script which uses pandoc to convert a md file to a pdf

## Prerequisites:
1. [Install LaTeX](https://www.latex-project.org/get/)
2. [Install pandoc](https://pandoc.org/installing.html)

## Installation
Move `pdfexporter`  script to the `/usr/local/bin` folder. Ensure the bash script is executable

```
mv pdfexporter /usr/local/bin
```

## Usage
You can run with just an input markdown file or specify the output. The output defaults to `out.pdf`

```shell
pdfexporter <path/to/md>
pdfexporter <path/to/md> -o <path/to/pdf>
```

You can print the help message by running the script with the `-h` flag

```shell
Create a pdf from a markdown file
usage: pdfexport <path/to/mdfile> [-d] <path/to/defaults> [-o] <path/to/pdfout>
Options:
  -h: Prints this usage message
  -d: Path to defaults file (default is defaults.yaml)
  -o: Path to output file (default is out.pdf)
  -y: Print YAML header for pandoc markdown conversions
```

### Defaults File
You can specify a defaults file, as defined in the [Pandoc spec](https://pandoc.org/MANUAL.html#default-files) . This allows you to use a header file and do some other configurations. For example:

```yaml
table-of-contents: true
number-sections: true
highlight-style: tango
include-in-header: header.tex
variables:
  fontsize: 11pt
  subgraph: true

```



