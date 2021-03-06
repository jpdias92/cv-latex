# CV Template in LaTeX

This is the 2 page CV template that I use for my own CV.

## Usage

### Compile inside a Docker container

#### Prerequisites

* Install [Docker](https://www.docker.com/) for your OS.

#### Generate the PDF

1. Pull the latest Docker image from Docker Hub, with `docker pull jpdias92/cv-template-latex`
   * Alternatively, build the image from the Dockerfile with `(cd docker;docker build -t jpdias92/cv-template-latex .)`
2. Compile the LaTeX source, inside a container, using lualatex (**recommended**): `./docker/latexdockercmd.sh latexmk -pdflatex=lualatex -cd -f -interaction=batchmode -pdf template.tex`
   * Alternatively, compile with xelatex: `./docker/latexdockercmd.sh latexmk -pdflatex=xelatex -cd -f -interaction=batchmode -pdf template.tex`

#### TeXstudio Integration

* [Mac](docs/docker_texstudio_integration.md#mac)

### Windows

1. Install [MiKTeX](https://miktex.org/howto/install-miktex), a TeX distribution for Windows that includes a large number of major packages.

2. Install an editor to edit and compile LaTeX documents. I recommend [TeXstudio](http://www.texstudio.org/) or [Texmaker](http://www.xm1math.net/texmaker/).

Once both the distribution and editor are installed, clone this repository using `git clone` and open the template.tex file in your editor. You're good to go!

## Troubleshooting

* [LaTeX Error: File '<foo_bar>' not found.](docs/troubleshooting.md#latex-error-file-ragged2esty-not-found)

## Built With

* [LaTeX](https://www.latex-project.org/)
* [Docker](https://www.docker.com/)
* [TeXstudio](http://www.texstudio.org/) - The IDE used

## Authors

**João Dias** - [jpdias92](https://github.com/jpdias92)

## Acknowledgments

[blang/latex-docker](https://github.com/blang/latex-docker) - Docker-based latex compilation

I've created this CV template based on many elements taken from several other templates, including:
* [Carmine Spagnuolo's Twenty Seconds Curriculum Vitae](https://github.com/spagnuolocarmine/TwentySecondsCurriculumVitae-LaTex)
* [Carmine Benedetto's Smart Fancy LaTeX CV](https://github.com/neoben/smart-fancy-latex-cv)
* [Adrien Friggeri's Fancy CV](https://www.sharelatex.com/templates/52fb8c1f33621a613683ecad)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details