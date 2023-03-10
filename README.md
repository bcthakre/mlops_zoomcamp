# mlops_zoomcamp
Running MLOPS Zoomcamp on GCP

# following tutorial is good to learn on how to 
# connect to GCE from VE Code

# https://youtu.be/y-l6FLSsCz0

# To create enviornment with conda

conda create -n <name_of_enviornment> python=3.9

# To activate enviornment

conda activate <name_of_enviornment>

# to install packages.

1. Create requirements.txt
2. do the following
pip install -r requirements.txt

if pip install requirements.txt does not work then do the following

cat requirements.txt | sed -e '/^\s*#.*$/d' -e '/^\s*$/d' | xargs -n 1 python -m pip install

# to check packages

pip list

# to run mlfow do the following inside the env

mlflow ui --backend-store-uri sqlite:///mlflow.db

The port at 5000 should be free, if not. Then run the following command

lsof -i :5000
and then
kill -9 <port_number>


