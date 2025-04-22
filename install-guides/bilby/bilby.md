# Bilby Installation Guide

This guide walks you through installing Bilby and its dependencies.

## Step 1: Create and activate a Conda environment

```bash
conda create -n bilby-env python=3.10
conda activate bilby-env
```

## Step 2: Install Bilby from source

```bash
- git clone https://git.ligo.org/lscsoft/bilby.git
- cd bilby/
- pip install -r requirements.txt
- pip install .
- cd ..
```