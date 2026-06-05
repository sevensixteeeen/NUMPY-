<h1 align="center">
<img src="https://raw.githubusercontent.com/numpy/numpy/main/branding/logo/primary/numpylogo.svg" width="300">
</h1><br>

[![Powered by NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](
https://numfocus.org)
[![PyPI Downloads](https://img.shields.io/pypi/dm/numpy.svg?label=PyPI%20downloads)](
https://pypi.org/project/numpy/)
[![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/numpy.svg?label=Conda%20downloads)](
https://anaconda.org/conda-forge/numpy)
[![Stack Overflow](https://img.shields.io/badge/stackoverflow-Ask%20questions-blue.svg)](
https://stackoverflow.com/questions/tagged/numpy)
[![Nature Paper](https://img.shields.io/badge/DOI-10.1038%2Fs41586--020--2649--2-blue)](
https://doi.org/10.1038/s41586-020-2649-2)
[![LFX Health Score](https://insights.linuxfoundation.org/api/badge/health-score?project=numpy)](https://insights.linuxfoundation.org/project/numpy)
[![OpenSSF Scorecard](https://api.securityscorecards.dev/projects/github.com/numpy/numpy/badge)](https://securityscorecards.dev/viewer/?uri=github.com/numpy/numpy)
[![Typing](https://img.shields.io/pypi/types/numpy)](https://pypi.org/project/numpy/)




<img width="953" height="327" alt="Screenshot 2026-03-10 222733" src="https://github.com/user-attachments/assets/1ca59482-d9f1-4e5c-aae5-c49e85fda07f" />


## What is NumPy?
NumPy is a Python library used for working with arrays.
It also has functions for working in domain of linear algebra, fourier transform, and matrices.
NumPy was created in 2005 by Travis Oliphant. It is an open source project and you can use it freely.
NumPy stands for Numerical Python.

## Why Use NumPy?
In Python we have lists that serve the purpose of arrays, but they are slow to process.
NumPy aims to provide an array object that is up to 50x faster than traditional Python lists.
The array object in NumPy is called ndarray, it provides a lot of supporting functions that make working with ndarray very easy.
Arrays are very frequently used in data science, where speed and resources are very important.

**Data Science:** is a branch of computer science where we study how to store, use and analyze data for deriving information from it.

## Why is NumPy Faster Than Lists?
NumPy arrays are stored at one continuous place in memory unlike lists, so processes can access and manipulate them very efficiently.
This behavior is called locality of reference in computer science.
This is the main reason why NumPy is faster than lists. Also it is optimized to work with latest CPU architectures.

## Which Language is NumPy written in?

NumPy is a Python library and is written partially in Python, but most of the parts that require fast computation are written in C or C++.


Youtube link: https://youtu.be/QUT1VHiLmmI

Discription: Python NumPy tutorail.

Learn the basics of the NumPy library in this tutorial for beginners. It provides background information on how NumPy works and how it compares to Python's Built-in lists. This video goes through how to write code with NumPy. It starts with the basics of creating arrays and then gets into more advanced stuff. The video covers creating arrays, indexing, math, statistics, reshaping, and more.


It provides:

- a powerful N-dimensional array object
- sophisticated (broadcasting) functions
- tools for integrating C/C++ and Fortran code
- useful linear algebra, Fourier transform, and random number capabilities

Testing:

NumPy requires `pytest` and `hypothesis`.  Tests can then be run after installation with:

    python -c "import numpy, sys; sys.exit(numpy.test() is False)"

Code of Conduct
----------------------

NumPy is a community-driven open source project developed by a diverse group of
[contributors](https://numpy.org/teams/). The NumPy leadership has made a strong
commitment to creating an open, inclusive, and positive community. Please read the
[NumPy Code of Conduct](https://numpy.org/code-of-conduct/) for guidance on how to interact
with others in a way that makes our community thrive.

Call for Contributions
----------------------

The NumPy project welcomes your expertise and enthusiasm!

Small improvements or fixes are always appreciated. If you are considering larger contributions
to the source code, please contact us through the [mailing
list](https://mail.python.org/mailman/listinfo/numpy-discussion) first.

Writing code isn’t the only way to contribute to NumPy. You can also:
- review pull requests
- help us stay on top of new and old issues
- develop tutorials, presentations, and other educational materials
- maintain and improve [our website](https://github.com/numpy/numpy.org)
- develop graphic design for our brand assets and promotional materials
- translate website content
- help with outreach and onboard new contributors
- write grant proposals and help with other fundraising efforts

For more information about the ways you can contribute to NumPy, visit [our website](https://numpy.org/contribute/). 
If you’re unsure where to start or how your skills fit in, reach out! You can
ask on the mailing list or here, on GitHub, by opening a new issue or leaving a
comment on a relevant issue that is already open.

Our preferred channels of communication are all public, but if you’d like to
speak to us in private first, contact our community coordinators at
numpy-team@googlegroups.com or on Slack (write numpy-team@googlegroups.com for
an invitation).

We also have a biweekly community call, details of which are announced on the
mailing list. You are very welcome to join.

If you are new to contributing to open source, [this
guide](https://opensource.guide/how-to-contribute/) helps explain why, what,
and how to successfully get involved.
