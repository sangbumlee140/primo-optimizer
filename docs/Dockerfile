# **IMPORTANT**: the following will most likely only work on Linux.
#
# From the `docs/` directory, run:
#
# ```sh
# docker build . -t primo/sphinx-latexpdf
# docker run --rm -v "$PWD":/docs primo/sphinx-latexpdf:latest
# ```
#
# The PDF will be in `_build/latex/primo.pdf`.

# we use :latest here instead of pinning an image tag since we want to
# simulate what happens on the ReadTheDocs runners
FROM sphinxdoc/sphinx-latexpdf:latest

WORKDIR /docs
RUN pip3 install sphinx_rtd_theme myst-parser[linkify] nbsphinx

CMD [ "make", "latexpdf" ]
