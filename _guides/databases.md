---
layout: main
title: Databases
category: data
---

## Databases vs. Spreadsheets

Transitioning to a web-based database from off-line spreadsheets can greatly improve the collection and management of datasets.  It also brings some overhead costs for setup and maintenance.

Below is a short summary of the differences between the two.

### Spreadsheets

* flexible
* quick to create
* intuitive

Spreadsheets are quick to set up, and easy to modify and share from person-to-person.  However, they become less useful when dealing with large or complex datasets.  While being easily read by a human, computers often have a harder time reliably reading spreadsheet data due to their flexible nature.

### Databases
* scalable 
* searchable with complex queries
* built-in data validation
* can capture relationships between variables

Databases are built to store large and complex datasets.  Database **queries** allow users to ask for specific subsets of the data that might be hard to extract from a spreadsheet, particularly if the data is spread across multiple spreadsheets.  For example, imagine trying to extract the following information from a collection of spreadsheets:

> Find all **Shareholders of Last Resort** who own 50% or more of a **Company** with copper deposits.

Or

> What percentage of **Glencore's** majority stake **Companies** have a community dialog platform?

Validation ensures that all input data is formatted correctly.  This be useful in the following cases:

* numbers are input as numbers and not words.  E.g. *1*, not *one*.
* input is limited to a specified number of options.  E.g. select one from: *active*, *inactive*, *canceled*, *unknown*.
* preventing duplicate entries 
* preventing mis-spellings


---

## CongoMines Data Model

The CongoMines database is built to store three categories of data: 

* **Mining Documents**
* **Mining Companies and Shareholding Companies**
* **Geographic data on mine projects**

This relationship can be summarized in the following diagram:

![]({{site.baseurl}}/img/db_schematic.png)

At the center are **Mining Companies** based in the DRC.  Companies can have multiple **Documents** in the document library that refer to them.  Companies can own or operate multiple **Mine Deposits**.  Companies can have **Shareholders** that own current or past shares in that company.
