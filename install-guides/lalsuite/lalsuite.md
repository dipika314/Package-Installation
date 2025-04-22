Steps to install any LALSuite in Conda environments:
1) Go to the directory where you want to clone the particular repo. (e.g /home/username/...)
2) git lfs install
3) clone the repo using 
git clone https://git.ligo.org/username/repo_name.git custom_name
(custom_name is the folder which will be created in the PWD. custom_name has the cloned repo files
4) go to the custom_name directory, which has the cloned repo
cd custom_name
#Building from source
5) Create a new environment using the environment.yml file
conda env create -f conda/environment.yml
By default, the name of the new environment will be lalsuite-dev. To change it, open the environment.yml file and change the name on the first row.
Let the name you created is env_name.
6) Activate the new environment
conda activate env_name
7) Define the installation directory (IDIR) for files of the repo, e.g
export IDIR=/home/username/opt/etc/env_name
8) Check if you are in correct branch
git branch
9) Checkout to a new branch if you want to work in that branch
git checkout branch_name
10) Configure, Make, Make Install
rm ${IDIR} -rf && ./00boot && ./configure --prefix=${IDIR} --enable-swig-python --enable-mpi --enable-openmp && make -j8 && make -j8 install
11) Source your installation to start using your LALSuite
source /home/username/opt/etc/env_name/lalsuite-user-env.sh
source /home/username/opt/etc/env_name/lalsuiterc
12) Logout, log back in and it should work.
