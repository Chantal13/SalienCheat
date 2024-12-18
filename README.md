# SalienCheat

👽 Cheating Salien minigame, the proper way.

## Table of Contents
1. [Introduction](#introduction)
2. [First Steps](#first-steps)
3. [PHP](#php)
    - [Windows](#windows-php)
    - [Mac](#mac-php)
    - [Linux](#linux-php)
4. [Python](#python)
    - [Windows](#windows-python)
    - [Linux/Cygwin](#linuxcygwin-python)
    - [Mac](#mac-python)
5. [Vagrant](#vagrant)
6. [Docker](#docker)

## Introduction
This repository provides scripts to cheat in the Salien minigame. Follow the instructions below to get started.

## First Steps
1. Join [SteamDB](https://steamcommunity.com/groups/SteamDB) (needed to represent captures).
2. Open [Salien Game Token](https://steamcommunity.com/saliengame/gettoken) and save it (<kbd>Ctrl</kbd>+<kbd>S</kbd>) as `token.txt` in the same folder as `cheat.php`.

## PHP

### Windows (PHP)
1. [Download this script](https://github.com/SteamDatabase/SalienCheat/archive/master.zip).
2. Extract it into a new folder.
3. Click `cheat.bat` and follow the instructions.

If that fails for any reason, or you still have questions, check out this [Google doc for commonly asked questions](https://docs.google.com/document/d/1DQx6K-SmfkF_fsy4sS-vMkUlqGrABolOpOtvAYaU3nU/prev).

### Mac (PHP)
1. (Optional) Launch the App Store and download any updates for macOS. Newer versions of macOS have PHP and curl included by default.
2. Extract the contents of this script to the Downloads folder.
3. Launch Terminal and run the script: `php downloads/cheat.php`.

You can also provide the token directly in CLI, to ease running multiple accounts:
```bash
php cheat.php token1 accountid1
php cheat.php token2 accountid2
```

### Linux (PHP)
1. Install `php-curl` and enable it in `php.ini`.
2. You know what you are doing. 🐧

## Python

⚠ **Python version currently does not support Boss battles, so you should choose the PHP version.** ⚠

### Windows (Python)
1. [Download this script](https://github.com/SteamDatabase/SalienCheat/archive/master.zip).
2. Extract it into a new folder.
3. Click `python-cheat.bat` and follow the instructions.

### Linux/Cygwin (Python)
1. (Optional) Setup virtual env: `virtualenv env && source env/bin/activate`.
2. Install required packages: `pip install requests tqdm`.
3. Run the script: `python cheat.py [token]`.

### Mac (Python)
1. (Optional) Launch the App Store and download any updates for macOS. Newer versions of macOS have Python 2.7.10 included by default.
2. Extract the contents of this script to the Downloads folder.
3. Launch Terminal and run the following scripts:
   1. `sudo easy_install pip`
   2. `pip install requests tqdm`
   3. `python downloads/cheat.py [token]`.

## Vagrant
1. Install [Vagrant](https://www.vagrantup.com/downloads.html) and [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
2. Run `vagrant up` to setup VM.
3. Run cheat:
   - For PHP: `vagrant ssh -c 'php cheat.php [token]'`.
   - For Python: `vagrant ssh -c 'python3 cheat.py [token]'`.

## Docker
1. Extract the contents of this script somewhere.
2. To build: `docker build . -t steamdb/saliencheat`.
3. To run: `docker run -it --init --rm -e TOKEN=<32 character token from gettoken url> steamdb/saliencheat`.
4. To stop running, press Ctrl+C.
