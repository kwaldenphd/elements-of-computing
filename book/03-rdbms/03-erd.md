# Entity Relationship Diagrams

An entity relationship diagram (sometimes called an ER Diagram or ERD) is a visual representation of tabular data structures that are linked as part of a database. 

We can think of an ERD and the entity-attribute-relationship framework as a type of conceptual model, something that makes sense for human users but may not match or map onto how the data is structured logically in tables or files.

Building an ERD requires understanding the underlying structure of your data, as well as how you want to create links across individual tables. ERDs have a specific vocabulary for describing database structure. In 1997, computer scientist Peter Chen outlined a natural language framework for building ER diagrams.

English Grammar Structure | ERD Structure
--- | ---
Common noun | Entity type
Proper noun | Entity
Transitive verb | Relationship type
Intransitive verb | Attribute type
Adjective | Attribute for entity
Adverb | Attribute for relationship

<blockquote>Peter Pin-Shan Chen, "English, Chinese and ER Diagrams," Data & Knowledge Engineering 23 (1997), 5-16. https://doi.org/10.1016/S0169-023X(97)00017-7</blockquote>

Let's break down each of those concepts:
- An ***entity*** is any abstract item in a computer program that can be given a unique name. Entities often have attributes.
- An ***attribute*** is a quality of an abstract entity expressed as a generalized category (e.g., “color” as an attribute of flowers). Attributes have values that vary with particular instances of the abstract entity they describe (e.g., the color “red” of a particular flower). Such attribute/value pairs can take the form of fields in a database or metadata tags or variables attached to objects in computer programs.
- A **relationship** is the connection or association (most commonly) between two entities.

## Entities

"A definable thing—-such as a person, object, concept or event-—that can have data stored about it. Think of entities as nouns. Examples: a customer, student, car or product." ([The components and features of an ER diagram,](https://www.lucidchart.com/pages/er-diagrams#section_3) LucidChart)

Entities are represented as rectangles in an ER Diagram.

## Attributes

"A property or characteristic of an entity." ([The components and features of an ER diagram,](https://www.lucidchart.com/pages/er-diagrams#section_3) LucidChart)

Attributes are represented as ovals in an ER Diagram.

## Relationships

"How entities act upon each other or are associated with each other. Think of relationships as verbs. For example, the named student might register for a course. The two entities would be the student and the course, and the relationship depicted is the act of enrolling." ([The components and features of an ER diagram,](https://www.lucidchart.com/pages/er-diagrams#section_3) LucidChart)

Relationships are represented as diamonds with lines that connect entity rectangles.

## Cardinality

"Defines the numerical attributes of the relationship between two entities or entity sets." ([The components and features of an ER diagram,](https://www.lucidchart.com/pages/er-diagrams#section_3) LucidChart)

Types of cardinality:

- One-to-one relationships
  * For example, each Notre Dame student has a unique ID number.
- One-to-many relationships
  * A single ND student registers for multiple courses.
- Many-to-many relationships
  * Multiple ND students work with multiple faculty members, and multiple faculty members work with multiple students.

The three main cardinal relationships:
- `one-to-one`
  * *one student associated with one mailing address*
- `one-to-many`
  * *one student registers for multiple courses, but all those courses have a single line back to that one student*
- `many-many`
  * *students as a group are associated with multiple faculty members, and faculty members in turn are associated with multiple students*

<p align="center"><img src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch3/cardinality.png?raw=true" width="1000"></p>

Cardinality is indicated through symbols added to the connecting lines of a relationship.

Visit Lucidchart's [What is an Entity Relationship Diagram (ERD)?](https://www.lucidchart.com/pages/er-diagrams#top) to learn more about the history, components, and limits of ER Diagrams.

## Application

Q1A: What entities are in the `players`, `teams`, `locations` and `transactions` tables? List the entitites by table and include some explanation of your thought process. If you're getting stuck, try describing the data included in each table using a sentence. Where are the nouns in each sentence?

Q1B: What attributes are in the `players`, `teams`, `locations` and `transactions` tables? What entities do these attributes describe? List the attributes by entity and table and include some explanation of your thought process. If you're getting stuck, go back to your list of entities from Q1A. What non-entity information in each table might describe an entity?

Q1C: What relationships do you see within and across entities in the `players`, `teams`, `locations` and `transactions` tables? What entities do these relationships connect? Include some explanation of your thought process. If you're getting stuck, go back to your list of entities from Q1B. How do these entities connect?

Q1D: Include the cardinality for the relationships you identified in Q1C. Include some explanation of your thought process.

Q1E: Build an ERD for the `players`, `teams`, `locations` and `transactions` tables. Include your diagram as well as an explanation of your process.

You can draw these by hand or use a drawing tool.

Free tools you can use to create ERDs:
- Free generic drawing tools:
  - [Google Drawings](https://docs.google.com/drawings) *Google Drive tool*
  - [Microsoft Paint](https://www.microsoft.com/en-us/p/paint-3d/9nblggh5fv99) *Windows users*
  - [MacOS Paintbrush](https://paintbrush.sourceforge.io/) *Mac users*
- Free online database-specific tools:
  - [ERDPlus](https://erdplus.com/)
    * *Prof. Walden's go-to tool!*
  - [LucidChart](https://www.lucidchart.com/pages/?anonId=0.1c8414ae17e41a83751)
  - [Visual Paradigm Online](https://online.visual-paradigm.com/diagrams/solutions/free-erd-tool/)