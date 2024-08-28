Kywy Documentation
-

KYWY is the python client to the KAWA data platform. 
You can use it to perform all the administrative tasks of your KAWA instance.
It also supports data analytics workloads: its lets you load data into KAWA and perform
computations from your Python runtime, benefitting from the scalability of your
data warehouse and from the security and governance of KAWA platform.

## Table of Contents
1. [Getting started](#1-getting-started)
2. [API Documentation](#2-api-documentation)


## 1 Getting started

### 1.a Configure credentials

Rename the `template.env` file to `.env` at the root of the kywy-documentation folder.
Fill out its content to match your installation. For example:

```bash
KAWA_API_URL=https://wayne.kawa.ai
KAWA_API_KEY=dsf4wFsrstgrsRSGrssrrghrts
KAWA_WORKSPACE=1
```

In order to obtain a valid `KAWA_API_KEY`, login into your KAWA instance, and refer to the screenshot below:

<p align="center">
  <img  src="readme-assets/api-key.png" alt="generate api key" />
</p>

**Make sure to use an admin account to perform all the administative tasks**. If you
want to use KYWY for data analytics workloads, any user profile will work.


### 1.b Install the kywy package

Run the following command in the venv of your choice:

`pip install kywy>=0.18.23`

You can then explore the content through jupyter-lab.
KYWY requires Python 3.10 or higher to run.


## 2 API Documentation

### 2.a The Data Loading API

The data loading API lets you send data to KAWA from your Python runtime.
One of its main objective is to let users write their own data loading logic to connect 
KAWA to internal APIs, custom file directory structures, in-house systems etc...

It supports both the pandas dataframe and the arrow tables for better performances.

This API has the following features:
- Create a datasource in KAWA
- Send panda dataframes or arrow tables to KAWA
- Configuration of primary keys and partitioning


Please refer to this [Notebook](./01_load_data_notebook.ipynb) for a detailed documentation and examples.


### 2.b The Computation API


