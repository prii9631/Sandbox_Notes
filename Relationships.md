/*Relationship between Objects*/

TYPE OF RELATIONSHIPS IN SALESFORCE

1. Lookup (One to Many)
2. Master-Detail (One to Many)
3. Self Lookup ( Lookup itself )
4. Many-to-many (Junction Object)
5. External
6. Indirect Lookup
7. Hierarchical

1. LOOKUP RELATIONSHIP

What it is:
A Lookup relationship is a loose connection between two objects. It’s like having someone’s business card - you know how to contact them, but you’re not dependent on them.

Characteristics:

* Optional connection - Child record can exist without a parent
* No cascade delete - Deleting parent doesn’t delete child records
* No roll-up summary fields - Can’t automatically calculate totals from child to parent
* Up to 40 lookup relationships per object
* Appears as a clickable link on the record 

Real-world Example:

Account 
 Contact: A contact might work for a company, but if the company record is deleted, the contact still exists
Opportunity 
 Campaign: An opportunity might be influenced by a campaign, but it's not dependent on it
 
2. MASTER-DETAIL RELATIONSHIP

What it is:
A Master-Detail relationship creates a tightly coupled parent-child connection. It's like a parent-child relationship where the child cannot exist without the parent.

CHARACTERISTICS:

* Required connection - Child record MUST have a parent
* Cascade delete - Deleting parent automatically deletes all child records
* Roll-up summary fields - Parent can show totals, counts, min/max from children
* Inherits security - Child records inherit sharing settings from parent
* Up to 2 master-detail relationships per object
* Cannot be optional - Always required

REAL-WORLD EXAMPLE:

Account 
 Invoice: An invoice must belong to an account; if account is deleted, invoices should be deleted too
Opportunity 
 Opportunity Line Items: Line items cannot exist without the opportunity
 
3. MANY-TO-MANY RELATIONSHIP (JUNCTION OBJECT)

What it is:
A Many-to-Many relationship connects two objects where each record in one object can relate to multiple records in another object, and vice versa.

HOW IT WORKS:

* Created using a Junction Object (custom object)
* Junction object has two Master-Detail relationships
* One to each of the objects you want to connect

CHARACTERISTICS:

* Flexible connections - Many records can relate to many other records
* Junction object holds the relationship data
* Both sides are masters - Junction object is detail to both
  
REAL-WORLD EXAMPLE:

Students 
 Classes: A student can take multiple classes, and each class can have multiple students
Doctors 
 Patients: A doctor can treat multiple patients, and a patient can see multiple doctors
 
4. HIERARCHICAL RELATIONSHIP

WHAT IT IS:

A Hierarchical relationship is a special lookup relationship that links an object to itself, creating a parent-child hierarchy.

CHARACTERISTICS:

* Self-referencing - Object relates to itself
* Creates tree structure - Like an organizational chart
* Up to 5 levels deep - Limited hierarchy depth
* Only available on User and custom objects

REAL-WORLD EXAMPLE:

User 
 Manager: Each user can have a manager who is also a user
Account 
 Parent Account: Companies can have parent companies
 
6. EXTERNAL RELATIONSHIP
   
External Object

An External Object in Salesforce is a virtual object that maps to data stored outside of Salesforce, allowing you to access and 
interact with external data as if it were native salesforce data without actually importing or storing it within your salesforce org.

The API name of the external object will always end with __x

What it is:

An External relationship is a relationship between the two External Objects based on a Unique ID
Link to External DB - https://orderdb.herokuapp.com/orders.svc/

CHARACTERISTICS:

* Links to external systems - Connects to data outside Salesforce
* Uses External ID - References external system's unique identifier
* Real-time data access - Can show external data without storing it
* Lightning Connect - Often used with external data sources
* 
REAL-WORLD EXAMPLE:

Salesforce Account ➞ ERP System Customer: Link Salesforce accounts to customer records in your ERP system

