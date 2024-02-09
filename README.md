# **SQL code annotations**
(Anotações de código SQL)

### UPDATEs in Database MYSQL:

##### UPDATE in MYSQL database table using JOIN.
>(UPDATE em tabela de banco de dados MYSQL com uso de JOIN.)
~~~sql
# Example:
UPDATE <table_1> AS tb1
LEFT JOIN <table_2> AS tb2 ON tb2.idTable_1 = tb1.id
SET tb1.time = tb2.time
WHERE tb2.id IN (1,2,3,4);
~~~

##### UPDATE in MYSQL database table using REPLACE.
>(UPDATE em tabela de banco de dados MYSQL com uso de REPLACE.)
~~~sql
# Example:
UPDATE <table_1> AS tb1 
SET tb1.attribute = REPLACE(tb1.attribute, <value_old>, <value_new>)
WHERE tb1.id IN (1,2,3,4);
~~~

### INSERTs in Database MYSQL:

##### INSERT in MYSQL database table using SELECT.
>(INSERT em tabela de banco de dados MYSQL com uso de SELECT.)
~~~sql
# Example:
INSERT INTO <TABLE_1> (<COLMUN_1>, <COLMUN_2>, <COLMUN_3>, <COLMUN_4>, <COLMUN_5>, <COLMUN_6>)
(
	SELECT t2.<COLMUN_1>, t2.<COLMUN_2>, t2.<COLMUN_3>, ... 
	FROM <TABLE_2> AS t2
	LEFT JOIN <TABLE_3> AS t3 ON t3.<COLMUN_x> = t2.<COLMUN_x>
	WHERE t3.<COLMUN_1> = t2.<COLMUN_1> AND t3.<COLMUN_2> = t2.<COLMUN_2>
	ORDER BY t2.<COLMUN_2> ASC
)
~~~

### SELECTs in Database MYSQL:

##### SELECT in MYSQL database table using REPLACE.
>(SELECT em tabela de banco de dados MYSQL com uso de REPLACE.)
~~~sql
# Example:
SELECT REPLACE(tb1.attribute, <value_old>, <value_new>) AS <alias>
FROM <table_1> AS tb1 
WHERE tb1.id IN (1,2,3,4);
~~~

##### SELECT in MYSQL database table using FIELD in ORDER BY.
>(SELECT em tabela de banco de dados MYSQL com uso de FIELD em ORDER BY.)
~~~sql
# Example:
SELECT tb1.<col1>, tb1.<col2>, tb1.<col3>
FROM <table_1> AS tb1 
WHERE tb1.<col1> > x;
order by FIELD(tb1.<col>,'C','A','D','B');
~~~

### **Auters**:

- [Anderson Miranda](https://github.com/aluipio)

### **Links Úteis**:

- [Python Brasil](https://python.org.br/)
