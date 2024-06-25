# Index
+ [What is Airflow](#airflow)
+ [Why Airflow](#why-airflow)
+ [Usecases](#usecases)
+ [Be aware of Airflow](#be-aware-of-airflow)


# airflow
Airflow is an open-source orchestration tool and platform for **authoring**, **scheduling** and **monitoring** workflows programmatically. On June 2, 2015, while Maxime Beauchemin was working for Airbnb, he released a [blog](#https://medium.com/airbnb-engineering/airflow-a-workflow-management-platform-46318b977fd8) introducing Apache [airflow](#https://github.com/apache/airflow) as an open source workflow management platform.


# Why Airflow 
After its release in 2015, it was a huge blast in the data community, and it's still the best open-source tool for data orchestration. But why? Well, there are several reasons. Some worth-mentioning features of airflow are:

- **Pipeline as Python**:  Data pipelines are created using Python, which is the de facto programming language for data.

- **Community Driven**: Open-source project backed by a large developer community. The github [repository](#https://github.com/apache/airflow) of Airflow has almost 3,000 contributors, and almost every month, new features are released.

- **Observability**: Its centralized UI provides awesome features to monitor and manage workflows easily. Also, we can set alerts to monitor critical issues. 

- **Data Aware Scheduling**: Data pipelines can be scheduled based on events that can also be set in airflow, e.g., files to arrive, new data to be arrived, etc.

- **Highly Extensible**: Airflow has more than 110 integration packages. Also, if you don't find the desired integration package, you can create your own by contributing to this open-source platform!

With these features, Airflow has become the central nervous system of today's modern data stack. To get some ideas about its popularity, Airflow has 30k+ people on its slack community, over 35k+ stars on the github repository, and over 9m+ monthly downloads. Companies like Walmart, Fanduel, Adobe, and the and the Texas Rangers use airflow on a daily basis. 

# Usecases
There are four (04) main use cases, where data is business critial, can be managed with airflow.

- **Data Powered Application**: In such applications, they expose dynamic data as key product features to function and provide value, e.g., fitness applications to provide health scores, activity goals, etc. 

- **Critical Operational Processes**: Refers to the essential workflows crucial for business functions like achieving business objectives and maintaining operational stability. For example, a fraud detection system for transactions in e-commerce applications.

- **Analytics & Reporting**: Involves the systematic analysis of data to derive insights, i.e.: Dashboards that influence decision. If any changes to the data occur or new data arrives, the dashboards must be updated.

- **MLOPs and AI**: MLOps involves the deployment and management of ML models within operational workflows. MLOps is the operational backbone for what end users receive as Artificial intelligence, for new entry.


In most of these use cases, latest data comes from different sources, like a smart watch or user-provided data from an app, must be gathered in a unified storage, transfered to specified format to be fit in other models or system and build reports and analytics. Here, airflow plays a vital role in creating a pipeline to ingest, transform, and backup data on a daily basis.

# Be aware of Airflow
There are three(03) main use cases while using airflow, when we may face some complications.

- **Streaming**: Airflow is designed for batch processing, not for streaming processing. Because until a run completes the next run can't be started in Airflow. That's why, it lacks the capability of real-time processing and immediate response to real-time data events. However, an alternative solution to this problem is using  ***airflow with Kafka***. Kafka is a tool to ingest and process data in real-time. Ingesting real-time data in the data warehouse using Kafka and then using the event data airflow can start workflows based on real-time data.

- **Scalibility**: On the availability of proper infrastructure, Airflow is scalable. Snapchat, Shopify, and Pinterest handle more than millions of monthly data using adequate infrastructure. But for small teams, with inadequate resources maintaining a complex infrastructure with airflow can challenging, and also some issues may arise.

- **Data Processing**: Though Airflow can process data with a resource-intensive system, but it wasn't mainly designed for it. So, with inadequate resources and infrastructure, some errors and issues may happen.

