conda activate env 
conda install -c conda-forge python-ldas-tools-framecpp
conda install -c conda-forge python-nds2-client

Install Bilby from source:
- git clone https://git.ligo.org/lscsoft/bilby.git
- cd bilby/
- pip install -r requirements.txt
- pip install .
- cd ..
