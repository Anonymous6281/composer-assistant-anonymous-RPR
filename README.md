# composers-assistant-REAPER
Welcome to the repository for Composer's Assistant scripts for REAPER. If you're looking for code for pretraining, finetuning, or evaluating Composer's Assistant models instead, click here: https://github.com/Anonymous6281/composer-assistant-anonymous

**The code in this repository will not work without the installation of at least one finetuned model. We are not distributing finetuned models at this time. We hope that this will change in the future. However, for now, you will have to pretrain and then finetune your own model (which may take a long time) using your own midi dataset using the code in the link above before the code in this repository will work for you.**

Please watch this video for audio examples and to learn how Composer's Assistant works: https://youtu.be/Zo_nqxSZKOw

**Installation instructions:**

First, install REAPER (64-bit): https://www.reaper.fm/

Second, install a 64-bit version of python 3.6 or higher: https://www.python.org/downloads/

Third, configure REAPER to see your python installation. (In REAPER, this is in the Options > Preferences > Plug-Ins > ReaScript menu)

Fourth, install the following three packages for your python installation: pytorch, transformers, and sentencepiece.

-Pytorch installation: Go to https://pytorch.org/ to get the command you need to run, then run this command from the command line. You'll want the stable build for your OS, using the "Pip" package for Python (NOT Conda). If you have an NVIDIA card, it is recommended to install a CUDA version. Otherwise, install the CPU version, which is a bit slower. The command you use should start with something like "pip3 install torch..."

-Transformers installation: From the command line, run ``pip install transformers``

-Sentencepiece installation: From the command line, run ``pip install sentencepiece``

Fifth, download and unzip the release (XXXXXXXXXXX) to your REAPER scripts folder. (To find your REAPER scripts folder, from within REAPER go to Options > Show REAPER resource path in explorer/finder..., and then open the folder called Scripts.) 

Your files are in the right place if you have files like

YOUR_PATH_TO_REAPER\Scripts\composer assistant\nn_server.py

and

YOUR_PATH_TO_REAPER\Scripts\composer assistant\CA_fill_empty_midi_items_in_time_selection.py

at this point.

Sixth, name your fineduned model(s) appropriately and place them in the provided models folder. In particular:

-If you are using a basic-vocabulary model, ensure that you have files 

YOUR_PATH_TO_REAPER\Scripts\composer assistant\models\unjoined_finetuned_model\model\pytorch_model.bin
YOUR_PATH_TO_REAPER\Scripts\composer assistant\models\unjoined_finetuned_model\model\config.json

in place. Aside from YOUR_PATH_TO_REAPER, everything MUST have the exact name and path as above.

-If you are using a joined-vocabulary model, ensure that you have files

YOUR_PATH_TO_REAPER\Scripts\composer assistant\models\spm_finetuned_model\model\pytorch_model.bin
YOUR_PATH_TO_REAPER\Scripts\composer assistant\models\spm_finetuned_model\model\config.json
YOUR_PATH_TO_REAPER\Scripts\composer assistant\models\spm_incl_note_duration_commands.model

in place. Aside from YOUR_PATH_TO_REAPER, everything MUST have the exact name and path as above.

You may install up to one joined-vocabulary model and one basic-vocabulary model. If you have both types of models installed, then our scripts will automatically choose whichever model is best for the task at hand.

From here, you load the scripts into REAPER in the usual way: In REAPER, go to Actions > Show action list..., then click on New action > Load ReaScript..., and then open all six scripts that start with "CA_". All other files are just helper files that these six scripts need to run. Before you run any of the scripts, start the neural net server by running the nn_server.py file in the download.

**How to cite Composer's Assistant:**

Coming Soon.
