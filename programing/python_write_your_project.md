# Write a Python package

### Developer Guide

- [LSST DM Developer Guide](https://developer.lsst.io)
	* Very valuable reference for developing and organizing codes for large research project.
	* [DM Python style guide](https://developer.lsst.io/python/style.html)

- Similarly, also see [SKA develop portal](https://developerskatelescopeorg.readthedocs.io/en/latest/) (Still under construction...)

### Structure

- "Dress for the job you want, not the job you have."

- [Structuring Your Project](https://docs.python-guide.org/writing/structure/)
	* From organizing files to the structure of the code, very good for beginners.
- [How To Package Your Python Code](https://python-packaging.readthedocs.io/en/latest/index.html)
	* Aims to put forth an opinionated and specific pattern to make trouble-free packages for community use
- [Cookiecutter - A logical, reasonably standardized, but flexible project structure for doing and sharing data science work](https://drivendata.github.io/cookiecutter-data-science/)

### Code Format

* It is good practice to follow well-established code format. Not only it can help you write codes that are nice looking and easy to maintain, it will help others to read and contribute to the code.
* For Python, [the __PEP8__ style guide](https://www.python.org/dev/peps/pep-0008/) is the most important one. Some of these rules feel unecessary and annoying, but there are always good reasons behind them.
- [__autopep8__: A tool that automatically formats Python code to conform to the PEP 8 style guide](https://github.com/hhatto/autopep8)
- [__black__: The uncompromising Python code formatter](https://github.com/python/black)
	* Blackened code looks the same regardless of the project you're reading. Formatting becomes transparent after a while and you can focus on the content instead.
- [__yapf__: A formatter for Python files from Google](https://github.com/google/yapf)

### Python setup.py file

- [A Human's Ultimate Guide to setup.py](https://github.com/kennethreitz/setup.py)
    - This is very good template for using __setup.py__

### Readme

- [Art of README](https://github.com/noffle/art-of-readme)
	- This is basically the only thing you need to study about writing a good readme file.
	- [Chinese version (中文版)](https://github.com/noffle/art-of-readme/blob/master/README-zh.md)

- [__readme-md-generator__ - CLI that generates beautiful README.md files](https://github.com/kefranabg/readme-md-generator)
	- __readme-md-generator__ will suggest you default answers by reading your package.json and git configuration.

### Document

#### General instructions

- [Writing change-controlled documentation](https://developer.lsst.io/project-docs/change-controlled-docs.html)
	* Manual provided by LSST DM team

- [LSST DM的Documenting Python APIs with Docstrings](https://developer.lsst.io/python/numpydoc.html#py-docstring-short-summary)
	* Also very good example by LSST DM. LSST adopts the __Numpydoc__ format.

#### Tools

- [__sphinx__ - Python documentation generator](https://www.sphinx-doc.org/en/1.5/index.html)
	* __Sphinx__ is a tool that makes it easy to create intelligent and beautiful documentation.
	* __Sphinx__ uses [__reStructuredText__](http://docutils.sourceforge.net/rst.html) as its markup language, and many of its strengths come from the power and straightforwardness of __reStructuredText__ and its parsing and translating suite, the [__Docutils__](http://docutils.sourceforge.net/).
	* [First steps with __sphinx__](https://www.sphinx-doc.org/en/1.5/tutorial.html)
	* [On __Markdown__ v.s. __reStructuredText__](https://gist.github.com/dupuy/1855764): __Markdown__ is easy to use; __reStructuredText__ is more extensible and powerful.
	* [Brandon’s __Sphinx__ Tutorial from PyCon 2013](https://buildmedia.readthedocs.org/media/pdf/brandons-sphinx-tutorial/latest/brandons-sphinx-tutorial.pdf)
	* [Sphinx Tutorial by Eric Holscher](https://sphinx-tutorial.readthedocs.io/start/) is the best place to start. The [GitHub repo itself](https://github.com/ericholscher/sphinx-tutorial) is a very good example.
	* [__Sphinx__ Themes](https://sphinx-themes.org/)

- [__pandoc__ - A universal document converter](https://pandoc.org/)
	* If you need to convert files from one markup format into another, __pandoc__ is your swiss-army knife. e.g. It can convert __reStructuredText__ to/from __Markdown__.

- [__rinohtype__ - The Python document processor](https://github.com/brechtm/rinohtype)
	* __Rinohtype__ is a document processor in the style of __LaTeX__. It renders structured documents to PDF based on a document template and a style sheet.
	* [A Simple Tutorial on How to document your __Python__ Project using __Sphinx__ and __Rinohtype__](https://medium.com/@richdayandnight/a-simple-tutorial-on-how-to-document-your-python-project-using-sphinx-and-rinohtype-177c22a15b5b)

- [__numpydoc__ -- Numpy's Sphinx extensions](https://github.com/numpy/numpydoc)
	* [The __numpydoc__ docstring format guide](https://numpydoc.readthedocs.io/en/latest/format.html)

- [__Doxygen__ - Generate documentation from source code](http://www.doxygen.nl/)
	* __Doxygen__ is the de facto standard tool for generating documentation from annotated C++ sources, but it also supports other popular programming languages such as C, Objective-C, C#, PHP, Java, Python, IDL.
	* [The __Doxygen__ document site for __Galsim__ is a very good example](http://galsim-developers.github.io/GalSim/index.html)

- [Read the Docs - Technical documentation lives here](https://readthedocs.org/)
	* Read the Docs simplifies software documentation by automating building, versioning, and hosting of your docs for you.

### Test

- [Testing Your Code from the Hitchhiker's Guide to Python](https://docs.python-guide.org/writing/tests/)
	* A nice summary of multiple approaches of unit test in Python.
- [Getting Started With Testing in Python from RealPython](https://realpython.com/python-testing/)
	* Another very nice introduction, convering __unittest__, __pytest__, and __nose__.

- [LSST DM: Python Unit Testing Guide](https://developer.lsst.io/python/testing.html)
	* LSST DM standard is a very good example：LSST tests should be written using the __unittest__ framework, with default test discovery, and should support being run using the __pytest__ test runner

- [__unittest__ — Unit testing framework](https://docs.python.org/3/library/unittest.html)
	* Basic unit test in Python. The [list of assertion methods is here](https://docs.python.org/3/library/unittest.html#assert-methods)

- [__pytest__ - helps you write better programs](https://docs.pytest.org/en/latest/)
	* The __pytest__ framework makes it easy to write small tests, yet scales to support complex functional testing for applications and libraries.
	* [Examples and customization tricks for __pytest__](https://docs.pytest.org/en/latest/example/): this is very useful.

-[__nose2__ - Nicer testing for Python](https://github.com/nose-devs/nose2)
	* __nose2__'s purpose is to extend unittest to make testing nicer and easier to understand. 

#### Code Coverage

- [Code coverage](https://en.wikipedia.org/wiki/Code_coverage): 

> In computer science, test coverage is a measure used to describe the degree to which the source code of a program is executed when a particular test suite runs. A program with high test coverage, measured as a percentage, has had more of its source code executed during testing, which suggests it has a lower chance of containing undetected software bugs compared to a program with low test coverage.  -- Wikipedia

- [__Coverage.py__ - Code coverage testing for Python](https://github.com/nedbat/coveragepy)
	* __Coverage.py__ measures code coverage, typically during test execution. It uses the code analysis tools and tracing hooks provided in the Python standard library to determine which lines are executable, and which have been executed.
	* [Quick start guide](https://coverage.readthedocs.io/en/v4.5.x/#quick-start)
	* [__pytest__ has a __pytest-cov__ plugin](https://pytest-cov.readthedocs.io/en/latest/)

- [__Codecov__ - Empower developers with tools to improve code quality and testing](https://github.com/codecov)
	* It is web service that improves your code review workflow and quality. Free for open source. Plans starting at $2.50/month per repository. You can login with your __GitHub__ or __Bitbucket__ account.	
	* [Here is a __Python__ example for __Codecov__](https://github.com/codecov/example-python)

### Optimization

- [Optimizing Python Code - Scipy Lecture Notes](http://www.scipy-lectures.org/advanced/optimizing/)
	* 1. Make it work; 2: Make it work reliably; 3: Optimization
	* No optimization without measuring: profiling and timing
	* Moving computation or memory allocation outside a for loop; Vectorizing for loops; Broadcasting;
	  Use in place operations; Be easy on the memory: use views, and not copies;

- [LSST DM Python performance profiling](https://developer.lsst.io/python/profiling.html)
	- Very good guide.

- [The Python Profilers](https://docs.python.org/3/library/profile.html)
	* Python comes with a series of profiling tools. The most useful ones are __cProfile__, __profile__, and __pstats__ (convert profiling results into a report)

- [Profiling Python using cProfile: a concrete case](https://julien.danjou.info/guide-to-python-profiling-cprofile-concrete-case-carbonara/)
	* __cProfile__ 对于发现程序中的瓶颈很有帮助

- [__line_profiler__ and __kernprof__ - Line-by-line profiling for Python](https://github.com/rkern/line_profiler)
	* __line_profiler__ is a module for doing line-by-line profiling of functions. __kernprof__ is a convenient script for running either line_profiler or the Python standard library's cProfile or profile modules, depending on what is available.
	* Can use __cProfile__ to identify "hotspot" (function that is the "bottleneck"), then use __line_profiler__ to exame the issue carefully.


#### Visualization

- [gprof2dot - Converts profiling output to a dot graph](https://github.com/jrfonseca/gprof2dot)
	* A general tool to convert different profiling software output to a dot graph.

- [__SnakeViz__ - An in-browser Python profile viewer](https://jiffyclub.github.io/snakeviz)
	* __SnakeViz__ is a viewer for Python profiling data that runs as a web application in your browser.

- [pycallgraph - Python module that creates call graphs for Python programs](https://github.com/gak/pycallgraph)
	* No longer maintained by the original author, but still available through a fork: [pycallgraph2](https://github.com/daneads/pycallgraph2)

