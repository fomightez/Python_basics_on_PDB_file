[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fomightez/BVCN-Jupyter_base/master?urlpath=lab%2Ftree%2FUntitled.ipynb)

# BVCN-Jupyter_base
JupyterLab 2.0 with offlinenotebook safety net and Visual Debugger for use via MyBInder.org by BVCN.

## Guidance on what you'll see in the sessions launched from here

#### Default notebook

The default notebook, 'Untitled.ipynb', that opens is a blank one with the debugger extension accessible. You can rename it and start coding. Save it back to you own local computer often via the `Download` button on the toolbar along the top of the notbeook. Alternatively, you can save the current version of the notebook to the remote server via `File` > `Save Notebook` and then download it to your local computer via `File` > `Download`. (That latter route is always available even if you are working elsewhere in Jupyter notebooks where you don't see the `Download` button on the toolbar. Note the toolbar `Download` button is a special convenience mechanism that doesn't require you to actually save to the remote machine first; however, saving to the remote machine often is a good habit as not all Jupyter systems you come across will have this convenient button.)

#### Safety net system

The safety net is there to allow recovery of any of your Jupyter notebook work if your MyBinder-served session times out, see [here](https://github.com/biovcnet/biovcnet.github.io/wiki/Infrastructure:-MyBinder#safety-net-for-the-ephemeral-nature-of-sessions). Look for the notebook 'safety net demo.ipynb' when the session starts. This 'safety net' system is actually the source of the toolbar `Download` button. Because it is a special extension added here, you won't see that special button on all Jupyter notebook sessions you come across in the wild.

#### Visual debugger

The Visual Debugger extension is there to allow you to step through and understand code that is running. You have to use the `xpython` kernel to have access to the debugger. What kernel us being used is indicated in the upper right above the running notebook. You'll either see a 'Python 3' or 'xpython' next to the indicator of whether code is being actively processed. If you are using the vanilla 'Python 3' kernel at present, you can switch kernels to use the debugger. Two ways to switch: 1) In the menubar select `Kernel` > `Change kernel...` and select `xpython` in the choice listing; or 2) left-click on the kernel name in the upper right and toggle the choice to `xpython`. Keep in mind that switching will clear the current computational 'state', and so you would need to run again any previously run code. To give you a sense of how to use the debugger, can see the [debugger demonstrated](https://github.com/jupyterlab/debugger#jupyterlabdebugger) in an animated gif [here](https://github.com/jupyterlab/debugger#jupyterlabdebugger). A notebook similar to the one in the demonstration gif is available in the running session as 'debugger demo.ipynb'.

----

## Technical details

Based on combining [the jupyter-offlinenotebook extension to enable saving notebooks to local-storage](https://github.com/manics/jupyter-offlinenotebook) and [the JupyterLab Visual Debugger](https://github.com/jupyterlab/debugger). This was tricky as adding `environment.yml` to the backbone of the jupyter-offlinenotebook extension repo kept causing the the jupyter-offlinenotebook extension to break. I had to move the necessary installs to the `postBuild` that was being used to install the jupyter-offlinenotebook extension.


-----

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fomightez/BVCN-Jupyter_base/master?urlpath=lab%2Ftree%2FUntitled.ipynb)