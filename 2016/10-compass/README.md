# October 2016: Compass

[Browse 2016](../README.md)

[Back to home](../../README.md)

Original PDF: [MDB_DN_2016_10_Compass.pdf](./MDB_DN_2016_10_Compass.pdf)

---
## Chapter 10. October 2016

Welcome to the October 2016 edition of MongoDB Developer’s Notebook (MDB-DN). This month we answer the following question(s); I am new to MongoDB, and am wondering what tools you offer for developers. Specfically, I am used to using a graphical tool for query plans, SQL style DML execution, data dictionary exploration (How do you deal with a jagged row table store ?), etcetera. What can you tell me ? Excellent question! The Enterprise Advanced license to MongoDB comes with at least three software components over and above the core database server. • MongoDB Compass is the component that you are effectively asking about, and the component we will detail in this document. • MongoDB Operations Manager (Ops Mgr) which is mostly similar to MongoDB Cloud Manager, is also for developers (and operations), and is centered more on provisioning and administering MongoDB. • And then MongoDB Connector for Business Intelligence (BI), is a middleware component that allows you to run SQL against a MongoDB server instance. We detailed the MongoDB Connector for BI in the March/2016 edition of this document.

The primary MongoDB software component used in this edition of MDB-DN is the MongoDB Compass, currently release1.4.0 beta-0. MongoDB Operations Manager (Ops Mgr), and/or MongoDB Cloud Manager are also great aids for developers (specifically the index advisor, provisioning, and monitoring tools), however; we have to reduce scope or this document would be many more pages.

All of the software referenced is available for download at the URL's specified, in either trial or community editions.

All of these solutions were developed and tested on a single tier CentOS 7.0 operating system, and a single tier MacOS operating system version 10.11.3, running in VMWare Fusion version 8.1 virtual machines. The MongoDB server software is version 3.311, and unless otherwise specified is running on one node, with no shards and no replicas. All software is 64 bit.

## 10.1 Terms and core concepts

As mentioned above, the focus of this edition of this document is developers, and the MongoDB Compass software component to the MongoDB Enterprise Advanced license. MongoDB Operations Manager (Ops Mgr), also has functionality aimed at developers, which we will list as out of scope for this document.

MongoDB Compass is a fat client (unlike a thin client, Web browser interface), and can be installed on MacOS and Windows 7 and higher. The download Url is here,

```text
https://www.mongodb.com/download-center?jmp=docs#compass
```

And the online documentation page and release notes are here,

```text
https://docs.mongodb.com/compass/
https://docs.mongodb.com/compass/release-notes/
```

## 10.1.1 MongoDB Compass Installation

The installation is ridiculously simple. In this document we are using release

1.4.0 beta-0. Similar to other MongoDB software products, the odd numbered releases tend to bring features, and the even numbered releases correct defects. Thus, the 1.4 release has no new customer facing features.

Figure 10-1 displays the release we are using in this document.

Figure 10-1 Release chain for MongoDB Compass.

Double-click the file image above, and follow the prompts. Example as displayed in Figure 10-2; just drag and drop the MongoDB Compass application to the Applications folder.

Figure 10-2 Installing MongoDB Compass on MacOS.

Figure 10-3 show various prompts you may witness in the install, and need to click though. In Figure 10-3, you are being informed that your connections history will be stored in file(s) located under your home directory, should you wish to cleanse later (delete history later).

Figure 10-3 Receiving various click though prompts.

## 10.1.2 MongoDB Compass Connection Preferences (Connecting)

After the install (and launch), you will receive the Connection Preferences dialog box, displayed in Figure 10-4.

Figure 10-4 Connection preferences dialog box, part of starting the Compass product.

In Figure 10-4, supply your connections preferences information, minimally the IP address and port of a given MongoDB database server instance, and Click Connect. This action leads to the display as shown in Figure 10-5.

> Note: The left side of this display will offer your connection history, to save re-entering this data when you re-enter the MongoDB Compass product.

Figure 10-5 Database and collections frame, left side of display.

## 10.1.3 MongoDB Compass, specifying the

current collection

Nearly there ! MongoDB Compass operates on collections (and views), and to do so we need first to choose a database and collection from the left side of the display. After selecting

```text
test_CM:zips
```

from the left panel, we are offered the display in Figure 10-6.

Figure 10-6 (Home page, of sorts), MongoDB Compass.

## 10.1.4 MongoDB Compass, Navigation Panel, Schema (TAB)

Relative to Figure 10-6, the following is offered:

- In addition to the four TABs (Schema, Documents, Explain Plan, Indexes), there is the Navigation Panel to the left. In the Navigation panel, the key features are to make current a new collection (or view), and call to refresh this list via the circular arrow icon in the upper right area of this pane. Should you have too many collections to manage in this panel, there is a Filter button, as shown.

- The Schema (TAB) was actually the original display from the version 1.0 of MongoDB Compass. The intent of this frame is to explore the contents of the current collection- • What key names are present. • What values and value types are present for each key. • Data distributions; how many of a given value are present. • Interactive query builder-

This area of the display is ‘hot’, meaning; as you click on given values for any of the keys, a query document is built in the address bar. The address bar displays a

```text
“{ }”
```

by default, the empty query document, as in, return all documents. The data types for a given key value are used to determine a chart type, that is; which type of visual control is best for a given type and distribution of data. In Figure 10-6, MongoDB Compass detected spatial data in the form of latitude and longitude, and rendered this data on a drag-able map. Very cool. Chart types are documented here,

```text
https://docs.mongodb.com/compass/understanding-charts/
```

> Note: This document is using version 1.4.0 beta-0 of MongoDB Compass. This version of Compass supports the cursor method.

```text
find( )
```

Version 1.5.0 of MongoDB Compass is expected to add support for the cursor method.

```text
aggregate( )
```

## 10.1.5 MongoDB Compass, Documents (TAB)

The Documents (TAB), displayed in Figure 10-7, allows you to edit individual documents, add documents and delete documents. The Documents TAB also shares the address bar with the Schema (TAB), so that you may more quickly highlight the given document that you wish to view or edit.

- A tool bar to the upper right of this display offers a pen (modify document), trash can (delete document), and copy/clone document (create a new document from an existing document as a source).

- A totally net new document insert is available via the Insert button.

- Notice too the overall collection set of statistics; number of documents in the collection, total document size, average document size, number of indexes, and more.

Figure 10-7 Documents (TAB), editing documents.

- Figure 10-8, displays the Documents (TAB) during a document edit. Notice that you can add keys, delete keys, and change the key value data type. How- Highlighting an existing key will offer an

```text
“X”
```

(delete) option in the left margin. The key value data type offers a drop down list box with valid key value types. Clicking after the last key in the collection offers a new key creation.

Figure 10-8 Documents (TAB) during a document edit.

## 10.1.6 MongoDB Compass, Explain Plan (TAB)

The June/2016 edition of this document provided a query primer; how to write queries with MongoDB. The May/2016 edition of this document detailed query optimizers, and how to tune queries; index negation, query shapes and processing patterns, predicate selectivity, and more.

The Explain Plan (TAB), displayed in Figure 10-9, offers a graphical interface to understand your query behavior.

In Figure 10-9, we have a single collection

```text
find( )
```

with an

```text
“$in”
```

expression. The collection access method is collection scan (“COLLSCAN”, sequential scan). 29 thousand documents were returned in 11 milliseconds. This query did not use an index to process the query document because no indexes were available to do so. (An index on

```text
test_CM.zips.state
```

could be a good idea here.)

Figure 10-9 MongoDB Compass, Explain Plan (TAB).

## 10.1.7 MongoDB Compass, Indexes (TAB)

In Figure 10-10, we display the Indexes (TAB) to MongoDB Compass. This panel is currently read-only, and displays any indexes in place on the current collection; keys, direction (ascending or descending), and whether a unique constraint is in place.

Figure 10-10 MongoDB Compass, Indexes (TAB).

## 10.2 In this document, we reviewed or created:

We detailed install and use of MongoDB Compass, a graphical client for programmers and administrators to execute queries, understand query plans and indexes, and perform the four primary SQL style data manipulation commands.

### Persons who help this month.

Dave Lutz, and Sam Weaver.

### Additional resources:

Free MongoDB training courses,

https://university.mongodb.com/

This document is located here,

```text
https://github.com/farrell0/MongoDB-Developers-Notebook
```
