Inserting Domains in IBM Maximo
==
This document provides instructions on how to insert domains into IBM Maximo using a database. It includes examples and formatting styles for different domain types.
==
Introduction
The objective of this document is to demonstrate the process of inserting domains into IBM Maximo through a database. Domains play a crucial role in defining and controlling the values that can be entered into specific fields within Maximo.

Summary
The following domain types will be covered in this document:
==
*ALNDOMAIN
*SYNONYMDOMAIN
*TABLE
*NUMERIC
*CROSSOVER
Each section will provide an example of how to insert the respective domain type.

ALNDOMAIN
To insert a domain of type ALNDOMAIN, execute the following SQL statement:


```
INSERT INTO ALNDOMAIN (DOMAINID, VALUE, DESCRIPTION, SITEID, ORGID, ALNDOMAINID, VALUEID)
VALUES ('POC', '1234', 'example', '', '', ALNDOMAINSEQ.NEXTVAL, 'POC|1234');
```

Note: In the above example, the SITEID and ORGID fields are left empty. However, you can fill them by enclosing their values in quotation marks within the INSERT statement.

To retrieve the sequence ID for ALNDOMAIN, use the following SQL query:

sql
Copy code
SELECT * FROM MAXSEQUENCE WHERE NAME LIKE '%ALNDOMAIN%';
Excel Integration
To integrate the ALNDOMAIN insert into Excel for multiple inserts, use the following formula:

excel
Copy code
POC --> ="INSERT INTO ALNDOMAIN (DOMAINID, VALUE, DESCRIPTION, SITEID, ORGID, ALNDOMAINID, VALUEID) VALUES ('ECIINMCODMT', '"&A2&"', '"&B2&"', '', '', ALNDOMAINSEQ.NEXTVAL, 'ECIINMCODMT|"&A2&"');"
Replace the values in cell A2 and B2 with the respective domain values in Excel, and the formula will generate the corresponding insert statement.

SYNONYMDOMAIN
// TODO: Add instructions and examples for SYNONYMDOMAIN

TABLE
// TODO: Add instructions and examples for TABLE

NUMERIC
// TODO: Add instructions and examples for NUMERIC

CROSSOVER
// TODO: Add instructions and examples for CROSSOVER

Feel free to update this document with instructions and examples for other domain types as needed.

Conclusion
By following the instructions provided in this document, you should now be able to successfully insert domains into IBM Maximo using a database. Remember to adapt the examples to your specific requirements and fill in any additional fields as necessary.



