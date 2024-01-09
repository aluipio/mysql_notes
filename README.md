# **SQL code annotations**
(Anotações de código SQL)

### UPDATE in Database MYSQL

>UPDATE in MYSQL database table using JOIN.
>(UPDATE em tabela de banco de dados MYSQL com uso de JOIN.)
~~~sql
# Example:
UPDATE <table_1> AS tb1
LEFT JOIN <table_2> AS tb2 ON tb2.idTable_1 = tb1.id
SET tb1.time = tb2.time
WHERE tb2.id IN (1,2,3,4);
~~~

### Auters:

- [Anderson Miranda](https://github.com/aluipio)

### **Links Úteis**

- [Python Brasil](https://python.org.br/)
