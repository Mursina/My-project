# Business Data Model API

- Find by attribute
http://localhost:8080/bonita/API/bdm/businessData/com.company.model.Student?q=findByBatch&p=0&c=3&f=Batch=E14

- Find by perrsistence Id
http://localhost:8080/bonita/API/bdm/businessData/com.company.model.Student/findByIds?ids=1,2,3,4


Some good readings
https://www.evoketechnologies.com/blog/custom-page-integration-bonita-bpm/
https://bonitatraining.com/bonita-bpm-7-developer-friendly-engaging-applications/

- call an attribute of JSON object
productDetail--> {product: tea, country: Sri Lanka} attribute of productDetail object can be called in UI as productDetail.country
productDetail--> [{product: tea, country: Sri Lanka}] attribute of productDetail object can be called in UI as productDetail[0].country

- h2 database update
create a text file and export the table as a CSV format

for example:
CREATE TABLE UPDATE AS 
select * from csvread('D:/Bonita/Course.txt',null,'charset=UTF-8 fieldSeparator=|')

INSERT INTO COURSEMODULE
SELECT * FROM UPDATE 

DROP TABLE IF EXISTS UPDATE