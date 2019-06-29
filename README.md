# maxima-tutorial-notebooks

*The Maxima Tutorial ported to use Jupyter notebooks*

## About

[Maxima](https://en.m.wikipedia.org/wiki/Maxima_(software)) is a computer algebra system that traces its lineage back to [MACSYMA](https://en.m.wikipedia.org/wiki/Macsyma), MIT, and the early days of Lisp. Stephen Wolfram was one of the biggest users of MACSYMA, which provided inspiration for Mathematica.

[Jupyter](https://en.m.wikipedia.org/wiki/Project_Jupyter) is a platform for interactive computing, including a notebook capability inspired by Mathematica notebooks. Language and system agnostic, Jupyter allows for any backend to be integrated.

The [maxima-jupyter](https://github.com/robert-dodier/maxima-jupyter) project is based on the Common Lisp Jupyter kernel and allows Maxima users to create and publish notebooks using their preferred computer algebra system.

## The Notebooks

This repository provides Jupyter notebooks for a portion of 
[The Computer Algebra Program Maxima - a Tutorial](http://maxima.sourceforge.net/docs/tutorial/en/gaertner-tutorial-revision/Contents.htm). It provides the following:
* [Getting Started](https://nbviewer.jupyter.org/github/calyau/maxima-tutorial-notebooks/blob/master/notebooks/Getting%20Started.ipynb)
* [First Steps with Maxima](https://nbviewer.jupyter.org/github/calyau/maxima-tutorial-notebooks/blob/master/notebooks/First%20Steps%20with%20Maxima.ipynb)
* [Maxima Tutorial - Symbolic Integration - First Examples](https://nbviewer.jupyter.org/github/calyau/maxima-tutorial-notebooks/blob/master/notebooks/Maxima%20Tutorial%20-%20Symbolic%20Integration%20-%20First%20Examples.ipynb)
* [Use of Lisp](https://nbviewer.jupyter.org/github/calyau/maxima-tutorial-notebooks/blob/master/notebooks/Use%20of%20Lisp.ipynb)

To run these locally, you may execute the following in a terminal (requires `git` and `docker` to be installed):

```sh
git clone git@github.com:calyau/maxima-tutorial-notebooks.git
cd maxima-tutorial-notebooks
docker run -it \
    -v `pwd`/notebooks:/home/oubiwann/maxima-jupyter/examples \
    -p 8888:8888 \
    calyau/maxima-jupyter \
    notebook --ip=0.0.0.0 --port=8888
```

Note that the above `docker` command is so useful that I have wrapped it in a shell script `start-maxima` and use it for all my computational maths projects.
