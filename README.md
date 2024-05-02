# Event-archetypes and literature references
The different types of events and literature references
<br>
<br>
*updated:*<br>
*02.05.2024: Initial version*
<br>

### Domain event
* The term domain event describes an occurrence of something that **happened in the business domain**. The concept originates in Domain-Driven Design (DDD). The event’s name usually already carries a lot of semantic meaning and is used within the domain language to describe the domain’s processes. [OTTO Consumer API Event Guidelines](https://api.otto.de/portal/guidelines/event-guidelines/concepts#domain-events)
* As a default practice, consider every domain event **"private", only meant for internal consumption**. Only through deliberate exposure consumers get access to the events, similar to how APIs are used instead of direct database access. [The different types of events in event-driven systems Frank de Jonge 2022](https://blog.frankdejonge.nl/the-different-types-of-events-in-event-driven-systems/)
* Examples of things that happen that might **not** be suitable to model as Domain Events:
    1. Something **technical** (a ButtonClicked, ExceptionThrown etc) happened that we want to record or handle, but it is not described in the ubiquitous language of our domain.
    2. Something that happened **outside of our bounded context**. This could a Domain Event in another system or a different bounded context. [What are Domain Events? Mattias Holmqvist 2020](https://web.archive.org/web/20221201162409/https://serialized.io/ddd/domain-event/)
* The terminology that is used for the aggregate’s name, its data members, its actions, and its **domain events** all should be formulated in the **bounded context’s ubiquitous language**. [Learning Domain-Driven Design. Aligning Software Architecture and Business Strategy (by Vlad Khononv 2021) p134](https://www.oreilly.com/library/view/learning-domain-driven-design/9781098100124/)
* 

___

### Data event
* Data events describe the **state of an entity at a specific moment in time**. They may be produced at a certain rate or if the state changes. Every data event at least contains the whole state of the entity but may also include the old state to allow consumers to detect changes. Data events do not contain the reason for the change. [OTTO Consumer API Event Guidelines](https://api.otto.de/portal/guidelines/event-guidelines/concepts#data-events)


___

### Data streams vs Event streams
* Wanneer gegevens over gebeurtenissen geen metadata bevatten spreken we over data en data streams (bijv. bij sensoren die alleen een pakket ruwe data leveren). Als er **wel contextgegevens** aanwezig spreken we over events en event streams (bijv. bij gebeurtenisgegevens die op basis van metakenmerken moeten worden geïnterpreteerd om verwerkt te kunnen worden). [Project Notificaties Architectuur p57](https://github.com/VNG-Realisatie/notificatieservices/blob/main/docs/achtergronddocumentatie/notificatieservices_architectuur.pdf)


___





