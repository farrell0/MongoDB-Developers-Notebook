MongoDB Developer's Notebook - Monthly Articles 2017
===================

| **[Monthly Articles - 2017](https://github.com/farrell0/MongoDB-Developers-Notebook/blob/master/README.md)**| **[Monthly Articles - 2016](https://github.com/farrell0/MongoDB-Developers-Notebook/blob/master/2016/README.md)**| **[Data Downloads](https://github.com/farrell0/MongoDB-Developers-Notebook/blob/master/data_download/README.md)** |
|-------------------------|--------------------------|-----------------|

This is a personal blog where we answer one or more questions each month from MongoDB customers in a non-official, non-warranted, non much of anything forum.

2017 May - -

>Customer:
>I’m coming from Oracle and MySQL, and can not possibly believe that you guys do not 
>support running SQL- As a developer or even operations person I need to run SQL to 
>understand my data, not to mention giving access to the data to my business intelligence 
>users. What can you tell me ?
>
>Daniel:
>Excellent question ! mongoDB has supported running SQL for some time, and with the 
>recent 2.1 release of our mongoDB Connector for Business Intelligence (BI Connector), 
>mongoDB’s capabilities in this area are even more performant.
>
>In this document we install, configure and use the version 2.1 BI Connector, and 
>install and use Eclipse, the Toad plugin for Eclipse, MySQL Workbench, a MySQL JDBC
>driver, Apache Drill, and more.
>
>In addition to running SQL, the October 2016 edition of this document details install, 
>configuration and use of the graphical query user interface to mongoDB, named mongoDB 
>Compass.
>
>[Download here](https://github.com/farrell0/MongoDB-Developers-Notebook/blob/master/articles/MDB_DN_2017_17_BiConnector2.pdf).

2017 April - -

>Customer:
>My company has a corporate campus with over 120 buildings, and an even larger number 
>of real time sensors; badge entry systems for doors, point of sale systems which we 
>can read, and more. One of the analytics routines we need to run associates a given 
>event with any other event at the same location and within a given amount of time. 
>Can you show me how to tie real time events to analytics routines inside mongoDB ?
>
>Daniel:
>In this document we deliver a Web form with real time streaming data from a finger 
>pulse meter. We use Python to read from the device, deliver the Web form, yadda.
>Honestly we used this device because it was the first we found with source code to
>read and graph the output in real time. (We didn't have a readily available door sensor.)
>If you choose not to purchase this device, we also simulate and output a data stream 
>from a pre-recorded ECG/EKG. (Net/net, this whole thing works whether you have a device
>or not.)
>
>Analytics- We found a number of articles describing analytics that can be performed
>on an ECG/EKG, in effect can I identify you from your ECG/EKG, but none of any consequence
>for a pulse meter. So, we moved the analytics you requested to a new data set that we 
>provide and detail.
>
>[Download here](https://github.com/farrell0/MongoDB-Developers-Notebook/blob/master/articles/MDB_DN_2017_16_IOT.pdf).
>
>[Resource Kit](https://github.com/farrell0/MongoDB-Developers-Notebook/blob/master/articles/MDB_DN_2017_16_IOT.tar),
>all of the programs used in this edition in Tar format.

2017 March - -

>Customer: 
>My company is committing to mongoDB in a large way. Over the years and with 
>prior technologies, we have built our own single pane of glass to monitor all of our 
>server systems; reporting server events, significant performance statistics, items to 
>watch for tuning, faults, and more. What does mongoDB offer in this area ?
>
>Daniel:
>We can’t promise we will cover every topic in this area as the basic question you ask 
>is essentially; tell me everything I need to know. We will, however, list many of our 
>favorites in the area of monitoring, statistics, tuning, and more. We detail; the mongoDB 
>Ops Mgr API, db.serverStatus(), audit logging, the message log file, the OpLog, query
>plans, index usage, and more.
>
>Where it makes sense we offer sample code. And in each case, we list the documentation 
>Url for further research as your specific needs and intents may suggest.
>
>[Download here](https://github.com/farrell0/MongoDB-Developers-Notebook/blob/master/articles/MDB_DN_2017_15_Monitoringb.pdf).

2017 February - -

>Customer:
>While we claim we sprint and scrum, my company wants to move from a traditional deployment 
>monolithic application architecture to a microservices architecture. We’ve looked at Docker 
>and others, and currently plan to go all in on Cloud Foundry. What can you tell me ?
>
>Daniel:
>In this article we overview the following topics; model-view-controller, stateful/stateless 
>applications, IaaS, PaaS, containers, application packaging (Gradle, Maven), Cloud Foundry, 
>services, user defined services, Cloud Foundry marketplace, and micro-services. We also
>detail all of the mongoDB themed Cloud Foundry marketplace tiles. 
>
>Then we install pcfdev, a laptop capable Cloud Foundry runtime, and deploy and scale a Python 
>Web application.
>
>[Download here](https://github.com/farrell0/MongoDB-Developers-Notebook/blob/master/articles/MDB_DN_2017_14b_CloudFoundry.pdf).

2017 January - -

>Customer:
>I really enjoyed the December/2016 edition of this document where you detailed the single 
>view use case, however; you left off Kafka as a topic, and while you ingested data from 
>multiple sources, you failed to detail how to get data out of mongoDB. What can you tell 
>me ?
>
>Daniel:
>In this article we continue our work from the December/2016 document, and add Kafka as a
>data source and target. And we read from the mongoDB OpLog to do that push into Kafka. The
>July/2016 edition of this document detailed the mongoDB Connector, which does this work 
>and more, but we wanted to demonstrate writing this code from scratch.
>
>[Download here](https://github.com/farrell0/MongoDB-Developers-Notebook/blob/master/articles/MDB_DN_2017_13_SingleView.pdf).
>
>[Resource Kit](https://github.com/farrell0/MongoDB-Developers-Notebook/blob/master/articles/MDB_DN_2017_13_SingleView.tar), all of the programs used in this edition in Tar format.
>
>This became part-two of a two part document. Part-one appears under December/2016.

If you are attending a Meetup group workshop on mongoDB Single View - -

>We are distributing a virtual machine; (Username/password, root password ). On Windows or 
>Linux you will need the free VMWare Player, available 
>[Download here](http://www.vmware.com/products/player/playerpro-evaluation.html). VMWare's Player product
>is not time-bombed, runs forever, yadda. There is no free VMWare Player for MAC, only a 
>for-charge product titled, VMWare Fusion. We've never tested it, however; Oracle VirtualBox 
>is supposed to be able to run this virtual machine. See this document for instructions on
>the topic running VMDKs from VirtualBox, 
>[Click here](https://github.com/farrell0/MongoDB-Developers-Notebook/blob/master/articles/OracleVirtualBoxToRunAVMDK.pdf). 
>Or, click this link for the source article, 
>[Click here](http://techathlon.com/how-to-run-a-vmdk-file-in-oracle-virtualbox/).
>
>Download the mongoDB Single View virtual machine here 
>[Click here (6 GB)](https://drive.google.com/file/d/0B37pFF1dJ894aEtRdEpCTnVKWTg). 
>This image was zipped up on Windows using 7-Zip.

