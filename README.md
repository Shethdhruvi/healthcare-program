# healthcare-program
Refer swagger UI for all REST API : http://localhost:8080/swagger-ui.html#/

Please go with below flow.

Enrolment

Create enrolment (add new enrolment) : POST /enrolment/add/enrollee
Update enrolment (update exisiting enrolment) : PUT /enrolment/update/enrollee/{id}
Get or View enrolment (view all enrolment or view enrolment by Id) : GET /enrolment/enrollee/{id} , GET /enrolment/enrollees
Delete enrolment (delete enrolment will also delete underlying dependents) : DELETE /enrolment/delete/enrollee/{id}
Depenedents

Create Depenedents (add new Depenedents) : POST /dependents/add/{enrolleeId}/dependents
Update Depenedents (update exisiting Depenedents) : PUT /dependents/update/dependents/{id}
Get or View Depenedents (view all Depenedents or view Depenedents by Id) : GET /dependents/dependents, GET /dependents/dependents/{dependentsId}
Delete Depenedents (it will delete Depenedents) : DELETE /dependents/delete/dependents/{id}
To run this application please follow below steps.

update mySql database properties in application.properties

spring.datasource.url=jdbc:mysql://localhost:3306/enrolment spring.datasource.username= spring.datasource.password=

Connect to MySql server and create database :

mysql -u root -p mysql> CREATE DATABASE enrolment;