<p align="left">
<a href="https://www.sspaeti.com/" target="_blank"><img src="https://sspaeti.com/images/sspaeti_quadrat.png" height="100"/></a>
</p>

# Practical Data Engineering Project

This is a practical example of a data engineering project with real-estates. The connected blog post about [Building a Data Engineering Project in 20 Minutes](https://www.sspaeti.com/blog/data-engineering-project-in-twenty-minutes/) you can find on my [website](https://sspaeti.com). Topics are:
<br>
* Getting the Data – Scraping with [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
* Storing on S3-[MinIO](https://min.io/)
* Custom Change Data Capture (CDC)
* Adding Database features to S3 – [Delta Lake](https://delta.io/) & [Spark](https://spark.apache.org/)
* Machine Learning part – [Jupyter Notebook](https://jupyter.org/)
* Ingesting Data Warehouse for low latency – [Apache Druid](https://druid.apache.org/)
* The UI with Dashboards and more – [Apache Superset](https://superset.apache.org/)
* Orchestrating everything together – [Dagster](https://dagster.io)
* DevOps engine – [Kubernetes](https://kubernetes.io/)
<br />

The Status of the project you find [here](https://github.com/orgs/sspaeti-com/projects/1).
<br /><br />
<img src="https://sspaeti.com/blog/the-location-independent-lifestyle/europe/sspaeti_com_todays_office_033.jpg" width="600">



## Starting Dagster

To get MinIO, Spark, Kubernetes, etc. ready, check the representive folder in [here](https://github.com/sspaeti-com/data-engineering-devops).

1. MinIO started
2. Kubernetes ready
3. Spark image and role and namespaces ready
4. cd `src/pipelines/real-estate` and start dagit with `dagit`

### Start issue

1. ImportError

```
ImportError: cannot import name 'SubscriptionObserver' from 'graphql_ws.gevent'
```

Manually install `graphql_ws` with version `0.3.1`.

```sh
pip install graphql_ws==0.3.1
```


2. dagster.check.CheckError

```
dagster.check.CheckError: Invariant failed. Description: Attempted to deserialize class "InstigatorState" which is not in the whitelist.
```


Use a clean dagster home.

``` sh
export DAGSTER_HOME="~/dagster-home-real-estate"
```

3. ModuleNotFoundError

```
ModuleNotFoundError: No module named 'bs4'
```

Install `bs4`

``` sh
pip install bs4
```

4. UserWarning

```
UserWarning: No dagster instance configuration file (dagster.yaml) found at /Users/zuzhi/dagster-home-real-estate.
```

Create an empty dagster.yaml file in /Users/zuzhi/dagster-home-real-estate.

```sh
touch ~/dagster-home-real-estate/dagster.yaml
```
