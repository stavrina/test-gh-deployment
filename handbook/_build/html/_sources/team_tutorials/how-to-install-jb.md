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
9.  Click `OK` to confirm the changes across all windows and you should be set!

## Conda on Git Bash

To check that Anaconda is properly installed on Git Bash follow the steps outlined below:
1. Open a Git Bash terminal
2. Type in `conda` and press return (<i class="bi bi-arrow-return-left"></i>)
3. If you get a menu like the one below then go to step 5, if not follow on from step 4
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
5. Anaconda sometimes will initialise the (base) environment whenever you open a new Git Bash (or any terminal), to stop this type:
   ```
   conda config --set auto_activate_base false
   ``` 
6. You are all set to go!

## (Optional) Pick your favourite IDE

Integrated Development Environments (IDE) can be a very personal thing. Over the years some of the people on our team have used several setups from [PyCharm](https://www.jetbrains.com/pycharm/) to text editors such as [Sublime Text](https://www.sublimetext.com/) or [Atom](https://atom.io/) accompanied by a detached terminal window. For what we demonstrate here we will use [Visual Studio Code](https://code.visualstudio.com/).
If you are comfortable with your set up we do not recommend you change anything.


## Install the Jupyter Book Environment

### Download and install the environment
(env-download-loc)=
Download the {{ jupyter_book }} environment by picture below, right-click and select `Save link as...`:  
**<a href="../required_packages/env.yaml" download>Anaconda Environment</a>**

1. Start up `Anaconda Navigator` (depending on your system this might take some time and open a few dialog boxes)
2. On the left-hand pane navigate to `Environments` (you might have to wait a bit again)
3. Next to the menu pane you will see the environments list, at the bottom you will see a menu with environment creating options, click `Import`
   :::{image} ../images/how-to-install-jb/conda-navigator-env.jpg
   :::
   An [animation](#import-gif) showing step 4-7 can be found below
4. Choose to **Import from:** your `Local drive`
5. Find the location where you saved the [environment](#env-download-loc) you saved from this page
6. (Optional) Specify a **New environment name:**
7. Click on **Import** and you are done, you just have to wait for all the packages to download
(import-gif)=
```{image} ../images/install-packages/anaconda-env.gif
:class: center
```
### Check that your environment works
The steps outlined below will help you check if you have installed the environment correctly:
1. Open up your **Terminal** application, we will use Git Bash to demonstrate
2. Type the following into your terminal application replacing `your-env-name` with the name you have defined for your environment:
   ```
   conda activate your-env-name
   ```
3. If you see your defined environment name above the terminal location enclosed by parentheses then your environment specification has worked!
4. (Bonus) Type the following to deactivate the environment:
   ```
   conda deactivate
   ```
   :::{image} ../images/how-to-install-jb/term-conda-activate-deactivate.gif
   :::

## Check that Jupyter Book works

You should have now have successfully installed all you need to get started with Jupyter Book, as outlined above. We will follow a simple exercise to test whether it runs on your machine.  
Open up a terminal and activate your environment as outlines in steps 1 - 3 [above](#check-that-your-environment-works), and type in the code below, press return (<i class="bi bi-arrow-return-left"></i>) and the Jupyter Book help menu should show appear:
```
jupyter-book
```
:::{image} ../images/how-to-install-jb/check-jb-install.gif
:::

## Clone the Repo and start contributing
You can find a condensed version in the [README]() accompanying the repository this handbook is hosted on.  

:::{warning}
The guide below assumes you have some familiarity with Git and branching. If not please follow one of the guides we recommend here.
:::

Follow these steps to clone the repository to your local drive and push updates:
1. Depending on if you have set up SSH-keys on your machine, or not, choose how you want to clone the repository on the page under the green `Code` button <span class="badge text-bg-success">Code <i class="bi bi-caret-down-fill"></i></span> and press the clone (<i class="fa-regular fa-clone"></i>) button to copy the line to your clipboard
   :::{hint}
   The most straightforward way is via HTTPS
   ::: 
2. Decided on a location (2 ways):
   1. Open up a terminal window and navigate to a directory you want to store this book in  
      **OR**
   2. Navigate to the directory (in File Explorer) you want to store this book in, right-click, and select `Git Bash here`
3. Type in, replacing `<text-you-copied>` with the actual text you copied:
   ```
   git clone <text-you-copied>
   ```
4. 






[^note-on-lsw]: Of course you can bypass most of this guide and use the Linux Subsystem on Windows and if you prefer `pip` as your package and virtual environment manager.
[^safari]: We are not able to test this on the Safari web browser, currently. If you are able to help feel free to contribute to this guide.