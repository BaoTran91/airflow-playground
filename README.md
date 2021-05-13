https://arpitrana.medium.com/install-airflow-on-macos-guide-fc66399b2a9e

#### CREATE ENV
conda create --name airflow-tutorial python=3.7

conda activate airflow-tutorial

export AIRFLOW_HOME=/Users/baotran/Desktop/airflow-tutorial

pip install apache-airflow

airflow db init

airflow webserver

airflow users create -r Admin -u admin -f xx -l bao -p baopw -e test@truedata.co

#### LOG INTO
http://0.0.0.0:8080