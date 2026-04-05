MongoDB Developer's Notebook - Monthly Articles 2017
===================

| **[Monthly Articles - 2017](./README.md)** | **[Monthly Articles - 2016](./2016/README.md)** | **[Data Downloads](./downloads/README.md)** | **[Legacy Data Files](./data_download/README.md)** |
|-------------------------|--------------------------|-----------------|-----------------|

This is a personal blog where we answer one or more questions each month from MongoDB customers in a non-official, non-warranted, non much of anything forum.

This site is no longer updated with new articles.

2017 January - -

>Customer:
>I really enjoyed the December 2016 edition of this document where you detailed the single view use case, however you left off Kafka as a topic, and while you ingested data from multiple sources, you failed to detail how to get data out of MongoDB. What can you tell me?
>
>Daniel:
>In this article we continue our work from the December 2016 document, add Kafka as a data source and target, and read from the MongoDB oplog to push into Kafka.
>
>[Read article](./2017/13-kafka-single-view/)
>
>[Original PDF](./2017/13-kafka-single-view/MDB_DN_2017_13_SingleView.pdf)
>
>[Resource Kit](./downloads/resource-kits-and-archives/MDB_DN_2017_13_SingleView.tar)
>
>[Part One](./2016/12-single-view/)

2017 February - -

>Customer:
>While we claim we sprint and scrum, my company wants to move from a traditional deployment monolithic application architecture to a microservices architecture. We’ve looked at Docker and others, and currently plan to go all in on Cloud Foundry. What can you tell me?
>
>Daniel:
>In this article we overview model-view-controller, stateful and stateless applications, IaaS, PaaS, containers, application packaging, Cloud Foundry, services, user defined services, marketplace tiles, and microservices. Then we install pcfdev and deploy and scale a Python Web application.
>
>[Read article](./2017/14-cloud-foundry/)
>
>[Original PDF](./2017/14-cloud-foundry/MDB_DN_2017_14b_CloudFoundry.pdf)

2017 March - -

>Customer:
>My company is committing to MongoDB in a large way. Over the years and with prior technologies, we have built our own single pane of glass to monitor all of our server systems; reporting server events, significant performance statistics, items to watch for tuning, faults, and more. What does MongoDB offer in this area?
>
>Daniel:
>We list many favorites in the area of monitoring, statistics, tuning, and more, including the Ops Manager API, db.serverStatus(), audit logging, the message log file, the oplog, query plans, index usage, and more.
>
>[Read article](./2017/15-monitoring/)
>
>[Original PDF](./2017/15-monitoring/MDB_DN_2017_15_Monitoringb.pdf)

2017 April - -

>Customer:
>My company has a corporate campus with over 120 buildings, and an even larger number of real time sensors; badge entry systems for doors, point of sale systems which we can read, and more. One of the analytics routines we need to run associates a given event with any other event at the same location and within a given amount of time. Can you show me how to tie real time events to analytics routines inside MongoDB?
>
>Daniel:
>In this document we deliver a Web form with real time streaming data from a finger pulse meter, and we also simulate and output a data stream from a prerecorded ECG/EKG. We then move the requested analytics to a new data set that we provide and detail.
>
>[Read article](./2017/16-iot/)
>
>[Original PDF](./2017/16-iot/MDB_DN_2017_16_IOT.pdf)
>
>[Resource Kit](./downloads/resource-kits-and-archives/MDB_DN_2017_16_IOT.tar)

2017 May - -

>Customer:
>I’m coming from Oracle and MySQL, and cannot possibly believe that you guys do not support running SQL. As a developer or even operations person I need to run SQL to understand my data, not to mention giving access to the data to my business intelligence users. What can you tell me?
>
>Daniel:
>MongoDB has supported running SQL for some time, and with the release of the 2.1 BI Connector, those capabilities are even more performant. In this document we install, configure and use the version 2.1 BI Connector along with Eclipse, Toad, MySQL Workbench, a MySQL JDBC driver, Apache Drill, and more.
>
>[Read article](./2017/17-bi-connector-2/)
>
>[Original PDF](./2017/17-bi-connector-2/MDB_DN_2017_17_BiConnector2.pdf)
>
>[Related article: Compass](./2016/10-compass/)

2017 June - -

>Customer:
>I need a hackathon for my MongoDB Meetup.com group, a skill set everyone can use like queries. Can you help?
>
>Daniel:
>The June 2016 edition of this document offers a primer on writing MongoDB queries, and the May 2016 edition details query tuning. In this edition we give you two data sets, US Postal codes and US airline performance data, and ask you to answer questions such as which city names are most common across states and whether an airline’s on-time claims are entirely truthful.
>
>[Read article](./2017/18-query-hackathon/)
>
>[Original PDF](./2017/18-query-hackathon/MDB_DN_2017_18_QueryHackathon.pdf)
>
>[Resource Kit](./downloads/resource-kits-and-archives/MDB_DN_2017_18_QueryHackathon.tar)
>
>[Related Slides](./downloads/slide-decks-and-supplemental-pdfs/MDB_DN_2017_18_QueryHackathon_slides.pdf)
>
>[Related article: Query Primer](./2016/06-query-primer/)
>
>[Related article: Index Tuning](./2016/05-index-tuning/)
>
>[Data downloads](./data_download/README.md)

For the 2016 archive and older companion material:

- [Browse the 2016 monthly articles](./2016/README.md)
- [Browse article companion downloads](./downloads/README.md)
- [Browse legacy shared data files](./data_download/README.md)
