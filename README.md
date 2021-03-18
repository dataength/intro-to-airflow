# Intro to Airflow

Apache Airflow คือ open-source แพลตฟอร์มที่เราสามารถเขียนโปรแกรมเพื่อควบคุม บริหารจัดการ ตั้งเวลางาน ขั้นตอนการประมวลผลต่างๆ ได้

### ความรู้พื้นฐาน

* ความรู้พื้นฐานในการใช้งาน Docker
* ความรู้พื้นฐานในการใช้งาน SQL
* ความรู้พื้นฐานในการเขียนโปรแกรมภาษา Python

### ติดตั้งบนเครื่อง

```sh
python -m venv ENV
source ENV/bin/activate
pip install --upgrade pip==20.2.4
export AIRFLOW_HOME=/Users/zkan/Projects/dataength/intro-to-airflow/airflow-local
./setup.sh
airflow db init
airflow users create \
    --role Admin \
    --username airflow \
    --password airflow \
    --firstname airflow \
    --lastname airflow \
    --email airflow@airflow.com
```

```sh
export AIRFLOW_HOME=/Users/zkan/Projects/dataength/intro-to-airflow/airflow-local
airflow webserver
```

```sh
export AIRFLOW_HOME=/Users/zkan/Projects/dataength/intro-to-airflow/airflow-local
airflow scheduler
```

### ติดตั้งแพคเกจเสริม

amazon
```sh
pip install apache-airflow-providers-amazon
```
