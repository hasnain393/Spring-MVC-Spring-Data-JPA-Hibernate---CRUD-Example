# Spring-MVC-Spring-Data-JPA-Hibernate---CRUD-Example

CREATE TABLE customer (
  id number(10) NOT NULL,
  name varchar2(45) NOT NULL,
  email varchar2(45) NOT NULL,
  address varchar2(45) NOT NULL,
  PRIMARY KEY (id)
);

-- Generate ID using sequence and trigger
CREATE SEQUENCE customer_seq START WITH 1 INCREMENT BY 1;

CREATE OR REPLACE TRIGGER customer_seq_tr
 BEFORE INSERT ON customer FOR EACH ROW
 WHEN (NEW.id IS NULL)
BEGIN
 SELECT customer_seq.NEXTVAL INTO :NEW.id FROM DUAL;
END;

Reference #https://www.codejava.net/frameworks/spring/spring-mvc-spring-data-jpa-hibernate-crud-example
Reference #https://www.youtube.com/watch?v=JfeCmn8NT88&feature=youtu.be

JPA Query-jpql for search
