# Contributing to this book
This guide is written using the {{ jupyter_book }} Python package.
If you are comfortable with Python, Git and Github feel free to fork our repository and start pushing content to it.  

:::{warning}
We assume that you are working on a managed Windows machine. Currently, the most straightforward way of using  {{ jupyter_book }} on Windows 10 has been Anaconda with a Python 3.7 version.
:::


You will find the necesary packages to for your build environment below:

* <a href="../required_packages/env.yml" download>Anaconda</a>
* <a href="../required_packages/requirements.txt" download>pip</a>


:::{attention}
For those of you who are a bit less familiar with the process we will go through it in the following pages
:::

<br>
<br>

:::{note}
The environment requirements files for creating a virtual environment using pip were created using the following command in a terminal window with the anaconda environment active:
```
pip list --format=freeze > requirements.txt
```
Similarly the Anaconda environment file you can import in Anaconda navigator was created using the following command:
```
conda env export > env.yaml
```
:::