# Get Anaconda
At the time of writing this, the Jupyter Book package has been tested with [Python 3.7 on Windows 10](https://jupyterbook.org/en/stable/advanced/windows.html)[^note-on-lsw], with the latest Python version being 3.10.  
We will use Anaconda as our package manager to specify which version of Python we want to run on.

## Download Anaconda
To download Anaconda, please visit the Anaconda [product page](https://www.anaconda.com/products/distribution), there you will find the appropriate distribution for your system. Usually, the download prompt shown below should have recognised your system, if not navigate to the [bottom of the page](https://www.anaconda.com/products/distribution#Downloads) or to the [Anaconda archive](https://repo.anaconda.com/archive/) to find the appropriate distribution for your system.

:::{attention}
We have tested downloading on Google Chrome, Microsoft Edge and Firefox Internet Browsers. On Chrome and Edge, it might appear as if the download did not start. However, if you navigate to menu (<i class="bi bi-three-dots-vertical"></i>) &rarr; downloads you will find the download progressing[^safari]. 
:::

(img-anaconda-download)=
```{figure} ../images/how-to-install-jb/anaconda-webpage-download.jpg
---
figclass: center
---
The Anaconda download display
```


## Install Anaconda
Locate the Anaconda installation file, this should be a `.exe` file if you are on Windows. Usually, it should be stored, by default settings in your internet browser, in the Downloads folder.

Steps:
1. Run the installer
2. Select `Next`
3. Select `I Agree` in the License Agreement
4. Select `Just Me` when prompted
5. It is recommended that you install Anaconda on your local, i.e. not connected to any network, drive, this is usually the `C:` drive for most University of Manchestert managed machines
:::{warning}
If you are using a machine provided by the University of Manchester do not install Anaconda on your `P:` drive or OneDrive
:::










[^note-on-lsw]: Of course you can bypass most of this guide and use the Linux Subsystem on Windows and if you prefer `pip` as your package and virtual environment manager.
[^safari]: We are not able to test this on the Safari web browser, currently. If you are able to help feel free to contribute to this guide.