INFORMATICS ENGINEERING DEPARTMENT ( _DEI_ ) ADVANCED TOPICS IN DATABASES 



# **Polyglot Persistence Project Smart Tourism Platform** 

# **1.** **_Context_** 

The project consists of developing a tourism platform in Python capable of integrating different database paradigms. The application must use at least three persistence systems: a relational database, a NoSQL database, and a vector database. A second NoSQL database may be used if technically justified. The objective is to understand how different types of data and access requirements may justify the use of different persistence solutions. The choice of technologies is free. It is up to the students to analyse the application requirements, choose the technologies they deem appropriate, and justify the decisions made. 

# **2.** **_Objectives_** 

- Þ This project aims to develop the ability to: 

- Þ work with different database paradigms; 

- Þ analyse data characteristics before choosing a persistence solution; 

- Þ model information according to the paradigm used; 

- Þ Integrate different persistence systems into a single application; 

- Þ justify modelling, architecture, and technology choice decisions; 

- Þ work with structured, semi-structured, geographic, and vector data; 

- Þ integrate embeddings into a persistence and search solution; 

- Þ use semantic search and recommendation mechanisms; 

- Þ analyse the impact of modelling and indexes on query performance; 

- Þ develop a Python application that integrates the different persistence systems. 

The use of various technologies, by itself, is not enough. The choices must be justified according to the needs of the application. 

# **3.** **_Application Description_** 

The application should represent a tourism platform where a user can search for and explore information related to tourist destinations. 

1 

INFORMATICS ENGINEERING DEPARTMENT ( _DEI_ ) ADVANCED TOPICS IN DATABASES 



Users should be possible to consult information about different destinations, perform searches, set preferences, and obtain results or recommendations tailored to the user's interests. 

The application should allow the implementation of a set of functionalities appropriate to the problem. 

The selection of functionalities to be implemented is the responsibility of the students and must be appropriate to the problem and duly justified. 

The interface should be a functional proof of concept, sufficient to use and demonstrate the main features of the application. 

The project's objective is not to evaluate the graphic or aesthetic quality of the interface. 

# **4.** **_Persistence requirements_** 

The information to be persisted in each database should be defined by the group, according to the characteristics of the data, the operations performed, and the respective paradigm. The distribution of information across different persistence systems must be technically justified. In the vector database, embeddings<sup>1</sup> associated with the application´s information must be generate, persist, index and used to support similarity searches. The model or method used to generate the embeddings is a matter of free choice and must be justified. There is no need to implement or train an embeddings model from scratch. The embeddings must be effectively persisted and used by the application through the similarity search mechanisms provided by this database. It is not sufficient to perform calculations and searches only in memory. 

# **5.** **_Application data_** 

The application should work with a suJiciently large dataset to allow for meaningful analysis of query performance and indexing mechanisms. The data should be suitable for the implemented functionalities and demonstrate the use of the persistence systems adopted in the project. DiJerent types of information should be considered, namely structured data, semistructured data, geographic information, preferences, interaction history, ratings, comments, and textual information used for semantic search. The distribution of this data across diJerent 

> 1 Embedding: a vector representation of information that preserves semantic relationships between data items, allowing similarity searches to be performed by comparing their positions in a vector space.  (https://www.ibm.com/think/topics/vector-embedding) 

2 

INFORMATICS ENGINEERING DEPARTMENT ( _DEI_ ) ADVANCED TOPICS IN DATABASES 



databases is an architectural and modelling decision that must be justified. Real-word data, public available data, synthetically generated data, or a combination thereof may be used, provided that the final set is suitable for the project. 

# **6. Application** **_Functionalities_** 

The application must implement a set of functionalities that demonstrate the integrated use of the persistence systems adopted in the project, namely: 

**Tourist Information** – users should be able to consult information about destinations, points of interest, and other content relevant to the tourism context. The information provided should be sufficiently rich to support the application´s other functionalities. 

**Geographic Exploration** - users should be able to consult location – based information and perform searches using geographic criteria. 

**User Profile -** The application should allow users to create and manage their profiles, defined preferences, save favourites destinations, and view their activity history. 

**Reviews -** users should be able to rate destinations and points of interest, as well as create, view and manage comments and reviews. 

**Natural Language Search** - The application must support searches expressed natural language. For example: “Museums to visit in Porto”; “Quiet beaches for families”, and “Traditional restaurants near the historic centre”. The search functionality musts rely on semantic search mechanisms **supported by the vector database.** 

**Recommendations** - The application should provide recommendations based on relevant information about users or the content viewed. The recommendations strategy adopted must be defined and justified. 

**Information Integration** - At least three different functionalities must integrate information originating from more than one database. At least one of these functionalities must involve the vector database through semantic search or recommendation mechanisms. 

The implementation of complex distributed real-time query mechanisms is not required. 

3 

INFORMATICS ENGINEERING DEPARTMENT ( _DEI_ ) ADVANCED TOPICS IN DATABASES 



# **_Tasks to be Developed_** 

# **_Part I - Definition of Schemas and Architecture_** 

This part involves defining the database schemas and the application architecture, focusing on the theoretical foundation, design decisions, and suitability to the system's needs. 

# **_A. Database Schemas and Data Models_** 

The data models used in the databases must be defined. 

It should be explained: 

- Þ what information is stored (persisted) in each database; 

- Þ how this information is organized; 

- Þ what relationships exist among the data; 

- Þ what operations are performed; 

- Þ what schema design patterns were considered and used, when applicable; 

- Þ what modelling decisions were made; 

- Þ how these decisions influence the performance, scalability, and maintenance of the solution. 

The distribution of information across different databases must be justified. 

There is no single correct solution. The important thing is that the choices made are appropriate for the problem and can be technically justified. 

# **_B. Application Architecture_** 

An architecture should be defined that clearly shows how the Python application communicates with the different persistence systems. 

The architecture should identify the main components of the application, the role of each database, and how the different systems interact with each other. 

4 

INFORMATICS ENGINEERING DEPARTMENT ( _DEI_ ) ADVANCED TOPICS IN DATABASES 



It should also explain how the data is distributed and how it is used to support the application´s main functionalities. 

The architectural choices should be justified taking into account the characteristics of the data, the types of operations performed, the performance, scalability, flexibility, consistency, and query complexity 

# **Part II – Application Implementation and Integration** 

# **A. The application must be implemented with the following characteristics:** 

- Þ **Functional Backend** - The backend must be able to integrate the persistence systems, performing read and write operations in the different systems, according to the needs of the data and the implemented functionalities. 

- Þ **Functional Frontend** - The frontend should be implemented as a functional proof of concept, allowing the user to interact with the application and use the system's main features. 

- Þ **Optimized Queries and Data Integration -** The system must include at least three distinct functionalities involving data from two or more databases. Queries must be optimized, considering the use of indexes and best practices for query optimization. 

- **B. Select three distinct scenarios,** corresponding to different databases, that allow the analysis of the circumstances under which the use of indexes can improve, or have little or no impact on, the performance of a query. The choices must be justified. 

# **Requirements:** 

- Þ A query in a relational database; 

- Þ A query in one of the NoSQL databases; 

- Þ A query in a vector database. 

# **For each scenario:** 

- Þ Describe the original query (without index); 

- Þ Create and apply the index(es) considered appropriate; 

5 

INFORMATICS ENGINEERING DEPARTMENT ( _DEI_ ) ADVANCED TOPICS IN DATABASES 



- Þ Present comparative results that allow for analysis of the impact of the indexes on performance, using, for example, execution time, query plan, logs, or benchmarking results; 

- Þ Explain why the selected indexes are effective or, when applicable, why their impact is limited or negligible. 

The queries must be related to the implemented functionalities and be representative of the realistic system usage. 

The objective is not only to show which indexes were created. The aim is to analyse in what circumstances an index is useful, when it may not bring relevant benefits, and justify the observed results. 

# **Deadlines and Deliverables** 

# **1- Discussion and Feedback on Database Schemas and Application Architecture:** 

**Week:** During Week 9, each group will participate in a discussion session with the professor regarding the proposed architecture and data modelling decisions (Part I). 

**Objective:** To allow the group to present the work developed up to week 9 and receive formative feedback on the modelling decisions, selected technologies, and proposed architecture. The discussion aims to identify possible issues and alternative approaches while the project is still under development. 

**Note:** This feedback does not constitute final approval of the proposed solution. Architectural and modelling decisions may be revised during the remainder of the project. 

**2- Final Delivery - Application Implementation and Part I Changes (if necessary)** 

**Delivery:** By 11:59 PM on December 8, 2026. 

**Objective:** Submission of a detailed report describing the revisions made to Part I following the feedback session, together with all tasks developed in Part II. 

6 

INFORMATICS ENGINEERING DEPARTMENT ( _DEI_ ) ADVANCED TOPICS IN DATABASES 



# **3- Oral Presentation:** 

**Date:** During weeks 13 and 14. 

**Objective:** Each group must present the work developed, discussing the implementation, technical decisions, and the analysis of indexing scenarios and their impact on query performance. 

# **Reports** 

Reports must be submitted in ZIP format. The ZIP file must follow the naming convention: ClassQ_Branch_xxxxxxx_yyyyyyy_zzzzzzz.ZIP, where: 

- Þ ClassQ – class name; 

- Þ Branch – name of the MEI specialization track; 

Þ xxxxxxx_yyyyyyy_zzzzzzz – student numbers. 

# **Penalties** 

- Þ Failure to comply with the submission deadline will result in a **10% penalty for each day of delay.** 

- Þ Any group member who is **not present** on the day and time of the presentation **will receive a grade of ZERO.** 

# **Use of Artificial Intelligence Tools** 

The use of **Artificial Intelligence (AI) tools** , including coding assistants, text generation tools, or other similar tools, is permitted as support for the **development of the project** , provided that it is used responsibly and transparently. 

The use of such tools **must be declared** . 

Assessment will focus on the **knowledge and skills acquired by the students** , and not solely on the artefacts produced. 

**Good work!!** 

7 

