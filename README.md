https://arpitrana.medium.com/install-airflow-on-macos-guide-fc66399b2a9e

#### CREATE ENV
conda create --name airflow-tutorial python=3.7

conda activate airflow-tutorial

export AIRFLOW_HOME=/Users/baotran/Desktop/airflow-tutorial

#### INSTALL AND START
pip install apache-airflow

airflow db init

airflow webserver

airflow users create -r Admin -u admin -f xx -l bao -p baopw -e test@truedata.co

#### LOG INTO
http://0.0.0.0:8080

https://airflow.apache.org/docs/apache-airflow/stable/tutorial.html

# initialize the database tables
airflow db init

# print the list of active DAGs
airflow dags list

# prints the list of tasks in the "tutorial" DAG
airflow tasks list tutorial

# prints the hierarchy of tasks in the "tutorial" DAG
airflow tasks list tutorial --tree

# command layout: command subcommand dag_id task_id date

# testing print_date
airflow tasks test tutorial print_date 2015-06-01

# testing sleep
airflow tasks test tutorial sleep 2015-06-01

# optional, start a web server in debug mode in the background
# airflow webserver --debug &

# start your backfill on a date range
airflow dags backfill tutorial \
    --start-date 2015-06-01 \
    --end-date 2015-06-07

