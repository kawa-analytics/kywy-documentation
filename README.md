# Kywy Documentation

KYWY is the python client to the KAWA data platform. 
You can use it to perform all the administrative tasks of your KAWA instance.
It also supports data analytics workloads: its lets you load data into KAWA and perform
computations from your Python runtime, benefitting from the scalability of your
data warehouse and from the security and governance of KAWA platform.

Here is the setup guide to get started with KYWY.


## 1 Configure credentials

Rename the `template.env` file to `.env` at the root of the kywy-documentation folder.
Fill out its content to match your installation. For example:

```bash
KAWA_API_URL=https://wayne.kawa.ai
KAWA_API_KEY=dsf4wFsrstgrsRSGrssrrghrts
KAWA_WORKSPACE=1
```

In order to obtain a valid KAWA_API_KEY, login into your KAWA instance, and refer to the screenshot below:

<p align="center">
  <img  src="readme-assets/api-key.png" alt="generate api key" />
</p>

**Make sure to use an admin account to perform all the administative tasks**. If you
want to use KYWY for data analytics workloads, any user profile will work.


## 2 Install the kywy package

Run the following command in the venv of your choice:

`pip install kywy>=0.18.23`

You can then explore the content through jupyter-lab.
KYWY requires Python 3.10 or higher to run.


