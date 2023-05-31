Introduction


The objetive of this document is show how to insert domains in ibm maximo across a database.

Summary
* ALNDOMAIN
* SYNONYMDOMAIN
* TABLE
* NUMERIC
* CROSSOVER

ALNDOMAIN 

INSERT INTO ALNDOMAIN (DOMAINID, VALUE, DESCRIPTION, SITEID, ORGID, ALNDOMAINID, VALUEID)
VALUES ('POC', '1234', 'example', '', '', ALNDOMAINSEQ.NEXTVAL, 'POC|1234');

In this example im not introducing SITEID and ORGID but this can be donned filled the ' (quotation marks) in the up insert.
The secuence id can be seen in the table maxsequence

SELECT * FROM MAXSEQUENCE WHERE NAME LIKE '%ALNDOMAIN%';

--Excel integration
This formula can be integrated in Excel for integrated with multiple inserts.

// poner esto en formato copy&paste
POC --> ="INSERT INTO ALNDOMAIN (DOMAINID, VALUE, DESCRIPTION, SITEID, ORGID, ALNDOMAINID, VALUEID) VALUES ('ECIINMCODMT', '"&A2&"', '"&B2&"', '', '', ALNDOMAINSEQ.NEXTVAL, 'ECIINMCODMT|"&A2&"');"


Decir que el dominio tiene que tener valores en maximo para poder añadir valores.
adjuntar fichero excel con ejemplo.

en vez de poc poner un dominio que exista en maximo.





