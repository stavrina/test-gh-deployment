# Get started with Jupyter Book

This guide is supposed to provide start to end instructions on contributing to this web-based handbook on Windows 10 OS. Feel free to read this out of sequence and focus on the sections that are relevant to you.

## Install Git Bash

## Get Anaconda
At the time of writing this, the Jupyter Book package has been tested with [Python 3.7 on Windows 10](https://jupyterbook.org/en/stable/advanced/windows.html)[^note-on-lsw], with the latest Python version being 3.10.  
We will use Anaconda as our package manager to specify which version of Python we want to run on.

### Download Anaconda
To download Anaconda, please visit the Anaconda [product page](https://www.anaconda.com/products/distribution), there you will find the appropriate distribution for your system. Usually, the download prompt shown below should have recognised your system, if not navigate to the [bottom of the page](https://www.anaconda.com/products/distribution#Downloads) or to the [Anaconda archive](https://repo.anaconda.com/archive/) to find the appropriate distribution for your system.

:::{attention}
We have tested downloading on Google Chrome, Microsoft Edge and Firefox Internet Browsers. On Chrome and Edge, it might appear as if the download did not start. However, if you navigate to menu (<i class="bi bi-three-dots-vertical"></i>) &rarr; downloads you will find the download progressing[^safari]. 
:::

(img-anaconda-download)=
```{image} ../images/how-to-install-jb/anaconda-webpage-download.jpg
:class: center
```

The Anaconda download display



### Install Anaconda
Locate the Anaconda installation file, this should be a `.exe` file if you are on Windows. Usually, it should be stored, by default settings in your internet browser, in the Downloads folder.

Steps:
1. Run the installer
2. Select `Next`
3. Select `I Agree` in the License Agreement
4. Select `Just Me` when prompted
5. Click `Next` on the Choose Install Location step
    :::{warning}
    Check that the Destination Folder is on your local drive, usuallly under `C:\Users\<username>\Anaconda3`.  
    It is recommended that you install Anaconda on your local, i.e. not connected to any network, drive, this is usually the `C:` drive for most University of Manchestert managed machines.  
    If you are using a machine provided by the University of Manchester do not install Anaconda on your `P:` drive or OneDrive
    :::
6. Do not add Anaconda to your PATH environment variables (we will do this later)
7. Check <i class="bi bi-check2-square"></i> the box prompting you to register Anaconda3 as your default Python 3.9 (optional but recommended unless you're planning to run multiple package managers)
8. Wait for Anaconda to finish installing and you are done!

### Edit your PATH environment variables

1. Begin with your Windows start menu (<i class="bi bi-windows"></i>)
2. Type in `env`, you should see `Edit the system environment variables` appear as the top option
3. Click on `Edit the system environment variables`
4. The `System Properties` window should pop up, navigate to the `Advanced` tab, if you're not already on it
5. At the bottom click on `Environment Variables...`
   ```{image} ../images/how-to-install-jb/env-var-edit.jpg
   ```
6. The `Environment Variables` window should open up, under `System variables` find `Path`
7. Highlight `Path` and click `Edit...`, the `Edit environment variable` window should open
8. Click `New` and type the path to your Anaconda3 installation directory, this is usually `C:\Users\<username>\Anaconda3`
   ```{image} ../images/how-to-install-jb/env-var-edit-path.jpg
   ```
9.  Click `Ok` to confirm the changes across all windows and you should be set!

## Conda on Git Bash

To check that Anaconda is properly installed on Git Bash follow the steps outlined below:
1. Open a Git Bash terminal
2. Type in `conda` and press return (<i class="bi bi-arrow-return-left"></i>)
3. If you get a menu like the one below then go to step [5](easy), if not follow on from step 4
   ```{image} ../images/how-to-install-jb/git-bash-conda-check.jpg
   ```
4. There are two ways you can proceed with this:
   1. First way:
      1. Open up `.bashrc` with your choice text editor (we will use notepad), this should be located in `C:\Users\<username>`
      2. If you can not locate you might need to turn on hidden file visibility:
         1. On the top ribbon pane of `File Explorer` head to the `View` tab and check the box with `Hidden items` next to it
            ```{image} ../images/how-to-install-jb/hidden-file-visibility.jpg
            ```
      3. In case the file does not exist open up notepad and save an empty file with the name `.bashrc` in your `C:\Users\<username>` directory
      4. Type `. /c/Users/<username>/Anaconda3/etc/profile.d/conda.sh` in your `.bashrc` file
   2. The second way:
      1. Open up Git Bash and type, replacing `<username>` with yours:
            ```
            echo '. /c/Users/<username>/Anaconda3/etc/profile.d/conda.sh' >> .bashrc
            ```
(easy)=
5. Anaconda sometimes will initialise the (base) environment whenever you open a new Git Bash (or any terminal), to stop this type:
   ```
   conda config --set auto_activate_base false
   ``` 
6. You are all set to go!

## (Optional) Pick your favourite IDE

Integrated Development Environments (IDE) can be a very personal thing. Over the years some of the people on our team have used several setups from [PyCharm](https://www.jetbrains.com/pycharm/) to text editors such as [Sublime Text](https://www.sublimetext.com/) or [Atom](https://atom.io/) accompanied by a detached terminal window. For what we demonstrate here we will use [Visual Studio Code](https://code.visualstudio.com/).
If you are comfortable with your set up we do not recommend you change anything.


## Install the Jupyter Book Environment

Download the {{ jupyter_book }} environment by picture below, right-click and select `Save link as...`:
- <a href="../required_packages/env.yaml" download>Anaconda Environment</a>


## Clone the Repo and start contributing
You can find a condensed version in the README accompanying the repository this handbook is hosted on






[^note-on-lsw]: Of course you can bypass most of this guide and use the Linux Subsystem on Windows and if you prefer `pip` as your package and virtual environment manager.
[^safari]: We are not able to test this on the Safari web browser, currently. If you are able to help feel free to contribute to this guide.