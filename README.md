# Royce Data Handbook

 This is a collection of guides, tutorials, and bits of information for the Royce Institute Data Infrastructure Project, we have written an extensive tutorial on how you can contribute which can be found [here].

## Usage

### Building the book

If you'd like to develop and/or build the Royce Data Handbook book, you should:

1. Clone this repository
2. Run `pip install -r requirements.txt` (it is recommended you do this within a virtual environment)
   1. Or `conda env create --file env.yaml`
3. (Optional) Edit the books source files located in the `handbook/` directory
4. (Optional) Run `jupyter-book clean handbook/` to remove any existing builds (Not recommended unless you are prepared to transfer files from `handbook` to `handbook/_build` in the hierarchical structure of this repository)
5. Run `jupyter-book build handbook/`

A fully-rendered HTML version of the book will be built in `handbook/_build/html/`.  
You can view the fully rendered HTML version locally by opening `index.html` located in `handbook/_build/html/` in your web browser.

### Hosting the book

Please see the [Jupyter Book documentation](https://jupyterbook.org/publish/web.html) to discover options for deploying a book online using services such as GitHub, GitLab, or Netlify.

For GitHub and GitLab deployment specifically, the [cookiecutter-jupyter-book](https://github.com/executablebooks/cookiecutter-jupyter-book) includes templates for, and information about, optional continuous integration (CI) workflow files to help easily and automatically deploy books online with GitHub or GitLab. For example, if you chose `github` for the `include_ci` cookiecutter option, your book template was created with a GitHub actions workflow file that, once pushed to GitHub, automatically renders and pushes your book to the `gh-pages` branch of your repo and hosts it on GitHub Pages when a push or pull request is made to the main branch.

## Contributors

We welcome and recognize all contributions. You can see a list of current contributors in the [contributors tab](https://github.com/Data-Curators-Royce-Institute/royce_data_handbook/graphs/contributors).

## Credits

This project is created using the excellent open source [Jupyter Book project](https://jupyterbook.org/) and the [executablebooks/cookiecutter-jupyter-book template](https://github.com/executablebooks/cookiecutter-jupyter-book).
