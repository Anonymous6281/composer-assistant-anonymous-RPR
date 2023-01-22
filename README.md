# composers-assistant-REAPER
Welcome to the repository for Composer's Assistant for REAPER. If you're looking for the repository for the academic version of this project instead, click here: https://github.com/Anonymous6281/composer-assistant-anonymous

Installation is a bit more involved than your average REAPER script. Before you attempt to install Composer's Assistant, please watch this video for audio examples and to learn how it works: https://youtu.be/Zo_nqxSZKOw

**Installation instructions:**

First, install REAPER (64-bit): https://www.reaper.fm/

Second, install a 64-bit version of python 3.6 or higher: https://www.python.org/downloads/

Third, configure REAPER to see your python installation. (In REAPER, this is in the Options > Preferences > Plug-Ins > ReaScript menu)

Fourth, install the following three packages for your python installation: pytorch, transformers, and sentencepiece.

-Pytorch installation: Go to https://pytorch.org/ to get the command you need to run, then run this command from the command line. You'll want the stable build for your OS, using the "Pip" package for Python (NOT Conda). If you have an NVIDIA card, it is recommended to install a CUDA version. Otherwise, install the CPU version, which is a bit slower. The command you use should start with something like "pip3 install torch..."

-Transformers installation: From the command line, run ``pip install transformers``

-Sentencepiece installation: From the command line, run ``pip install sentencepiece``

Fifth, download and unzip the release (https://github.com/Anonymous6281/composer-assistant-anonymous-RPR/releases/download/v1.0.0/composers-assistant-for-REAPER-v1.0.0.zip) to your REAPER scripts folder. (To find your REAPER scripts folder, from within REAPER go to Options > Show REAPER resource path in explorer/finder..., and then open the folder called Scripts.) It is highly recommended that you unzip to a folder *within* your scripts folder instead of dumping everything directly into the scripts folder, but it's up to you.

From here, you load the scripts into REAPER in the usual way: In REAPER, go to Actions > Show action list..., then click on New action > Load ReaScript..., and then open all six scripts that start with "CA_". Ignore the other files. They are just helper files that these six scripts need to run. Before you run any of the scripts, start the neural net server by running the nn_server.py file in the download.

**Note:**

Composer's Assistant for REAPER was created to test the feasibility of using machine learning models in an interactive manner in the composition process. The weights in the models it uses are research artifacts, and should be treated as such.

**How to cite Composer's Assistant:**

Coming Soon.
