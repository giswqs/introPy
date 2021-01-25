# Installation
This pages describes how to download and install the software and materials needed for this course.

## Python
For this course, we need a working installation of Python. There are two options: you can download Python yourself (see below) or you can use an online environment preconfigured with a working Python installlation. 

### Online access to Python
For students of the Research Master Psychology, we have set up an external server with Python (through [Jupyterhub](https://jupyter.org/hub), which is explained [here](jupyter.md)) which can be used to do the tutorials of week 1; so no need to download Python yourself. The course's Canvas page outlines how to access the server. Alternatively, you may use [Binder](https://mybinder.org/), which is a service that provides an online Python environment with the course's materials. Note that our own Jupyterhub instance is only accessible to students from the Research Master Psychology who are enrolled in the "Programming for Psychology" course. Note that you must be connected to UvA VPN to be able to access the UvA server.

The tutorials of week 1 are embedded on this website as well (i.e., the pages on the left with the `(T)`), but these are not interactive, i.e., you cannot add, edit, or run the code. To start the tutorials as interactive notebooks, click on the "rocket" button on the top right and choose *JupyterHub* (UvA students only) or *Binder* (anyone). This will launch an online environment in which you can interactively run the material. Note that the "rocket" button is only available for actual tutorials.

In the online environment, you'll see a lot of files. The course material is stored in the *tutorials* folder. The *solutions* folder contains the same material, but with solutions to the exercises in the tutorials. You can ignore the rest of the files (which have to do with configuration and the contents of this website).

:::{warning}
Note that Binder does not save your notebooks! After you quit Binder (or it times out after an hour of inactivity), all progress is lost (but you can download your notebooks/files). Our own Jupyterhub *does* save the files.
:::

More information on how to get started with the tutorials, go to the [week 1 page](../week_1/python.md).

### Installing Python on your own computer
If you want to install Python on your own computer, we *highly* recommend you install Python through the [Anaconda distribution](https://www.anaconda.com/products/individual). In the box below, you can find detailed installation instructions (thanks to [the Netherlands eScience Center](https://escience-academy.github.io/2020-12-07-parallel-python/)) specific to your operating system (Mac, Windows, or Linux).

```{tabbed} Mac

1. Open the [Anaconda download page](https://www.anaconda.com/products/individual#download-section) with your web browser;
2. Download the Anaconda Installer with Python 3 for macOS (you can either use the Graphical or the Command Line Installer);
3. Install Python 3 by running the Anaconda Installer using all of the defaults for installation.

For a more detailed instruction, check out the video below:

<iframe width="560" height="315" src="https://www.youtube.com/embed/TcSAln46u9U" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{tabbed} Windows

1. Open the [Anaconda download page](https://www.anaconda.com/products/individual#download-section) with your web browser;
2. Download the Anaconda for Windows installer with Python 3. (If you are not sure which version to choose, you probably want the 64-bit Graphical Installer Anaconda3-...-Windows-x86_64.exe);
3. Install Python 3 by running the Anaconda Installer, using all of the defaults for installation except **make sure to check Add Anaconda to my PATH environment variable**.

For a more detailed instruction, check out the video below:

<iframe width="560" height="315" src="https://www.youtube.com/embed/xxQ0mzZ8UvA" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

**Note**: the video tells you to use *git bash* to test your Python installation; you may ignore this. As explained below, Windows users should use the *Anaconda prompt* instead.
```

After you have installed your own Python distribution, you can check whether it is working correctly by opening a terminal (on Mac/Linux) or Anaconda Prompt (on Windows) and running the following:

```
python -c "import sys; print(sys.executable)"
```

This command should print out the location where you installed Python, e.g., `/Users/your_name/anaconda3/bin/python` (on Mac) or `C:\Users\your_name\anaconda3\bin\python` (on Windows). 

## PsychoPy
In the second week of the course, we are going to use [PsychoPy](https://www.psychopy.org/), a Python-based software package, to create simple experiments. There are two ways of installing PsychoPy: installing the core Python package `psychopy` and installing the complete "standalone" PsychoPy software package. If you have a working version of Python already, the `psychopy` Python package can be installed as a regular third-party package through [pip](https://packaging.python.org/tutorials/installing-packages/) &mdash; the **P**ackage **I**nstaller for **P**ython. However, because PsychoPy interacts with a lot of (non-Python) programs and components, getting the core `psychopy` package to work properly is all but trivial. Instead, we *highly* recommend installing the ["standalone" version of PsychoPy](https://www.psychopy.org/download.html). The standalone version does not only contain a working version of the `psychopy` package, but also a custom Python distribution specifically designed to work with PsychoPy, as well as a neat code editor and even a graphical interface (the PsychoPy *Builder* interface) to create experiments without programming.

:::{warning}
For some (?) Windows users, the PsychoPy website states "To install PsychoPy on Windows we recommend" installing PsychoPy through `pip`. Don't do this (because it doesn't include the Builder interface). Instead, click on the link [PsychoPy releases on github](https://github.com/psychopy/psychopy/releases) and download the latest `.exe` file (currently, `StandalonePsychoPy3-2020.2.10-win64.exe`).
:::

:::{note}
Note that PsychoPy does not work on remote servers (including our own and Binder/colab instances), so students from the Research Master course should also download the [standalone PsychoPy version](https://www.psychopy.org/).
:::

To test whether the installation was successful and everything works as expected do the following:

* Start PsychoPy (this should open three windows);
* Make sure you are in the *PsychoPy Builder* window;
* In the menu, click *Demos* &rarr; *Unpack demos*, and select a location to unpack the demo experiment files;
* Click on *Demos* again and then on *stroop*, which should open `stroop.psyexp` in the PsychoPy Builder;
* Click on the green "play" button (*run experiment*);
* After a couple of seconds, you should see a pop-up prompting for a "session" and "participant number";
* Fill in some number (e.g., 01) and click on *Ok* to start the experiment;
* Your screen should turn black and start the experiment!

## Downloading the material
We use [Jupyter notebooks](https://jupyter.org/) for our tutorials. The materials are stored on [Github](https://github.com/lukassnoek/introPy) and can be downloaded as a zip-file by clicking on the link below:

[Download materials](https://github.com/lukassnoek/introPy/archive/master.zip)

After downloading the materials, please unzip the folder. The resulting directory has the following structure and contents (the # symbols represent comments/information):

```
intropy                        # Directory root
│                        
├── LICENSE                                      
├── README.md
├── build_book
│
├── intropy                    # Directory with materials
│   │
│   ├── _build                 #
│   ├── _config.yml            #
│   ├── _toc.yml               #
│   ├── config                 #
│   ├── getting_started        #
│   ├── gradebook.db           #
│   ├── img                    #
│   ├── index.md               #
│   ├── misc                   #
│   ├── nbgrader_config.py     #
│   ├── references.bib         #
│   │
│   ├── solutions              # Tutorials WITH solutions
│   │   ├── week_1             # Jupyter notebook tutorials
│   │   └── week_2             # Files + solutions of PsychoPy tutorials
│   │       ├── Builder
│   │       └── Coder
│   │
│   ├── tutorials              # Tutorials
│   │   ├── week_1             # Jupyter notebook tutorials
│   │   └── week_2             # Files needed for PsychoPy tutorials
│   │       ├── Builder
│   │       └── Coder
│   │
│   ├── week_1                 # Website pages week 1 (can be ignored)
│   └── week_2                 # Website pages week 2 (can be ignored)
│
├── requirements.txt           # Required packages for week 1 (and book)
└── test_material              # Test Jupyter notebooks (for developers)
```

The only revelant directories are the `intropy/intropy/solutions` and `intropy/intropy/tutorials` directories, which contain the tutorials with and without solutions included, respectively.

Note that students from the Research Master course do *not* need the materials from week 1 (which are already on the server), only the materials from week 2 (because PsychoPy programs need to be run locally on your computer).

:::{warning}
If you work with your own Python installation, you need to install additional Python packages to make sure all material from week 1 works as expected. To do so, open a terminal (Mac/Linux) or Anaconda prompt (Windows)
and navigate to the root directory of the downloaded materials (`cd path/to/downloaded/materials`) and run the following:

    pip install -r requirements.txt

Note that this is not necessary if you use Binder (or the UvA JupyterHub) as your Python environment!
:::

Before you start working on the course materials, read the next page on the [Jupyter ecosystem](jupyter.md).