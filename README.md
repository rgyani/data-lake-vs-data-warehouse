# data-lake-vs-data-warehouse


The “data” part of the terms “data lake,” “data warehouse,” and “database” is easy enough to understand.  
Data is everywhere, and the bits need to be kept somewhere. But should they be stored in a data warehouse, a data lake, or an old-fashioned database?  
It all depends on how that data is going to be used.

It’s difficult to define the names precisely because they are tossed around colloquially by developers as they figure out the best way to store the data and answer questions about it. All three forms share the goal of being able to squirrel away bits so that the right questions are answered quickly.

Still, the terms have evolved and taken on relatively standard meanings.

### What is a database?
The database now means both the software that stores and manages the information as well as the information stored within the database. Developers use the word database with some precision to mean a collection of data, because the software needs to know that orders are kept on one machine and the addresses on another.

Users rarely know where the values are kept and may just call the entire system the database. And that’s fine — most software development is about hiding that level of detail. Among databases, the relational database has become a workhorse for much corporate computing. The classic format arranges the data in columns and rows that form tables, and the tables are simplified by splitting the data into as many tables and sub-tables as needed. Good relational databases add indexes to make searching the tables faster. They can employ SQL and use sophisticated planning to simplify repeated elements and produce concise reports as quickly as possible.

Lately, non-relational types of databases have gained traction. These so-called NoSQL databases don’t store the data in relational tables. They are often chosen when developers want the flexibility to add new fields or elements for some entries but not others.

But there are use cases where the database is not enough.


### What is a data warehouse?
The data warehouse is a collection of databases, although some may use less structured formats for raw log files. The idea of a data warehouse evolved as a consequence of businesses establishing long-term storage of the information that accumulates each day, and to meet the need to report on and analyze that data.

Building a data warehouse is more than just choosing a database and a structure for the tables, as it requires creating retention policies. Data warehouses often include sophisticated analytics to generate statistics to study changes over time. Data warehouses are often tightly integrated with graphics routines that produce dashboards and infographics to quickly show changes in the data.

Generally, the term data warehouse has come to describe a relatively sophisticated and unified system that often imposes some order upon the information before storing it.

### What is a data lake?
A data lake takes a different approach to building out long-term storage from a data warehouse. In modern data processing, **a data lake stores more raw data for future modeling and analysis, while a data warehouse typically applies a relational schema to the information before it’s stored**. The data lake may not even use databases to store the information because the extra processing required isn’t worth it. The data is stored in flat files or logs.

Lakes are better choices for storing large amounts of records in case someone wants access to a few or many of them in the future. Regulatory compliance is a common use case.

Some use both metaphors for the same system. The incoming raw data is stored in the data lake and, after some analysis and aggregation, the information often finds a home in the data warehouse.

### What are some examples?
Databases, warehouses and lakes take many forms because businesses have many, different needs for historical record keeping. The choices a business makes for keeping these records affects the architecture and structure. Here are several hypothetical examples:

* _A Drop-Shipping Company_. They sell gadgets online and outsource fulfillment to others. They use a basic database to track orders and often discard records not long after the orders have been delivered. Their products change frequently and so they feel they have no need for historical data.
* _A Doctor’s Office._ The medical industry has elaborate regulations to protect patient privacy. They use a special service to store patient records that can offer long-term retrieval for queries that may come years later. The service acts like a lake because the doctor and the patients are not involved in any research that might involve comparing and contrasting outcomes from treatment. The service can just store and retrieve, not analyze.
* _A Manufacturing Company._ The company has a dominant position in a stable industry that requires them to make smart decisions about long-term trends in sales and pricing. They need to compare sales by region over time to make commitments for opening and refurbishing plants and physical warehouses. Managing this supply chain is much easier with a sophisticated data warehouse able to run complex queries.
* _A Network Security Group._ The routers and switches collect plenty of raw data about the packets traveling across the network in case someone wants to analyze any anomalies. These raw values are stored in a big data lake for several weeks until they’re no longer needed. If no unusual events occur, the data is disposed of without being analyzed.
* _A Drug Research Company._ The company gathers raw data about drug trials and also compiles aggregated reports for regulation. The company wants to retain the data, perhaps indefinitely, to aid future researchers and satisfy any questions from regulators. It uses a data lake to collect the initial raw information and a warehouse to store aggregated reports.

| Characteristics |	Data Warehouse | Data Lake |
|-----------------|----------------|-----------|
| Data	| Relational from transactional systems, operational databases, and line of business applications |	Non-relational and relational from IoT devices, web sites, mobile apps, social media, and corporate applications |
| Schema |	Designed prior to the DW implementation (schema-on-write) |	Written at the time of analysis (schema-on-read) |
| Price/Performance |	Fastest query results using higher cost storage	| Query results getting faster using low-cost storage |
| Data Quality | Highly curated data that serves as the central version of the truth |	Any data that may or may not be curated (ie. raw data) |
| Users |	Business analysts | Data scientists, Data developers, and Business analysts (using curated data) |
| Analytics |	Batch reporting, BI and visualizations | Machine Learning, Predictive analytics, data discovery and profiling |
