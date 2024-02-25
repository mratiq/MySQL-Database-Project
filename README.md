# Foobar

Foobar is a Python library for dealing with word pluralization.

## Q-1. Write an SQL query to fetch “FIRST_NAME” from the Worker table using the alias name <WORKER_NAME>.



```bash
Select FIRST_NAME AS WORKER_NAME from Worker;
```


```
+-------------+
| WORKER_NAME |
+-------------+
| Monika      |
| Niharika    |
| Vishal      |
| Amitabh     |
| Vivek       |
| Vipul       |
| Satish      |
| Geetika     |
+-------------+
```
## Q-2. Write an SQL query to fetch “FIRST_NAME” from the Worker table in upper case.

```
Select upper(FIRST_NAME) from Worker;
```
```bash
+-------------------+
| upper(FIRST_NAME) |
+-------------------+
| MONIKA            |
| NIHARIKA          |
| VISHAL            |
| AMITABH           |
| VIVEK             |
| VIPUL             |
| SATISH            |
| GEETIKA           |
+-------------------+
```
## Q-3. Write an SQL query to fetch unique values of DEPARTMENT from the Worker table.

```
Select distinct DEPARTMENT from Worker;
```

```
+------------+
| DEPARTMENT |
+------------+
| HR         |
| Admin      |
| Account    |
+------------+
```

## Q-4. Write an SQL query to print the first three characters of  FIRST_NAME from the Worker table.

```
 Select substring(FIRST_NAME,1,3) from Worker; 
```
```
+---------------------------+
| substring(FIRST_NAME,1,3) |
+---------------------------+
| Mon                       |
| Nih                       |
| Vis                       |
| Ami                       |
| Viv                       |
| Vip                       |
| Sat                       |
| Gee                       |
+---------------------------+
```
## Q-5. Write an SQL query to find the position of the alphabet (‘a’) in the first name column ‘Amitabh’ from the Worker table.

```
Select INSTR(FIRST_NAME, BINARY'a') from Worker where FIRST_NAME = 'Amitabh';
```
```
+------------------------------+
| INSTR(FIRST_NAME, BINARY'a') |
+------------------------------+
|                            1 |
+------------------------------+
```

## Q-6. Write an SQL query to print the FIRST_NAME from the Worker table after removing white spaces from the right side.

```
Select RTRIM(FIRST_NAME) from Worker;
```

```
+-------------------+
| RTRIM(FIRST_NAME) |
+-------------------+
| Monika            |
| Niharika          |
| Vishal            |
| Amitabh           |
| Vivek             |
| Vipul             |
| Satish            |
| Geetika           |
+-------------------+
```
## Q-7. Write an SQL query to print the DEPARTMENT from the Worker table after removing white spaces from the left side.

```
Select LTRIM(DEPARTMENT) from Worker;
```

```
+-------------------+
| LTRIM(DEPARTMENT) |
+-------------------+
| HR                |
| Admin             |
| HR                |
| Admin             |
| Admin             |
| Account           |
| Account           |
| Admin             |
+-------------------+
```

## Q-8. Write an SQL query that fetches the unique values of DEPARTMENT from the Worker table and prints its length.

```
Select distinct length(DEPARTMENT), department from Worker;
```
```
+--------------------+------------+
| length(DEPARTMENT) | department |
+--------------------+------------+
|                  2 | HR         |
|                  5 | Admin      |
|                  7 | Account    |
+--------------------+------------+
```

## Q-9. Write an SQL query to print the FIRST_NAME from the Worker table after replacing ‘a’ with ‘A’.

```
Select first_name, REPLACE(FIRST_NAME,'a','A') from Worker;
```
```
+------------+-----------------------------+
| first_name | REPLACE(FIRST_NAME,'a','A') |
+------------+-----------------------------+
| Monika     | MonikA                      |
| Niharika   | NihArikA                    |
| Vishal     | VishAl                      |
| Amitabh    | AmitAbh                     |
| Vivek      | Vivek                       |
| Vipul      | Vipul                       |
| Satish     | SAtish                      |
| Geetika    | GeetikA                     |
+------------+-----------------------------+
```
## Q-10. Write an SQL query to print the FIRST_NAME and LAST_NAME from the Worker table into a single column COMPLETE_NAME. A space char should separate them.

```
Select FIRST_NAME,LAST_NAME, CONCAT(FIRST_NAME, ' ', LAST_NAME) AS 'COMPLETE_NAME' from Worker;
```

```
+------------+-----------+-----------------+
| FIRST_NAME | LAST_NAME | COMPLETE_NAME   |
+------------+-----------+-----------------+
| Monika     | Arora     | Monika Arora    |
| Niharika   | Verma     | Niharika Verma  |
| Vishal     | Singhal   | Vishal Singhal  |
| Amitabh    | Singh     | Amitabh Singh   |
| Vivek      | Bhati     | Vivek Bhati     |
| Vipul      | Diwan     | Vipul Diwan     |
| Satish     | Kumar     | Satish Kumar    |
| Geetika    | Chauhan   | Geetika Chauhan |
+------------+-----------+-----------------+
```

## Q-11. Write an SQL query to print all Worker details from the Worker table order by FIRST_NAME Ascending.

```
Select * from Worker order by FIRST_NAME asc;
```
```
+-----------+------------+-----------+--------+---------------------+------------+
| WORKER_ID | FIRST_NAME | LAST_NAME | SALARY | JOINING_DATE        | DEPARTMENT |
+-----------+------------+-----------+--------+---------------------+------------+
|         4 | Amitabh    | Singh     | 500000 | 2021-02-20 09:00:00 | Admin      |
|         8 | Geetika    | Chauhan   |  90000 | 2021-04-11 09:00:00 | Admin      |
|         1 | Monika     | Arora     | 100000 | 2021-02-20 09:00:00 | HR         |
|         2 | Niharika   | Verma     |  80000 | 2021-06-11 09:00:00 | Admin      |
|         7 | Satish     | Kumar     |  75000 | 2021-01-20 09:00:00 | Account    |
|         6 | Vipul      | Diwan     | 200000 | 2021-06-11 09:00:00 | Account    |
|         3 | Vishal     | Singhal   | 300000 | 2021-02-20 09:00:00 | HR         |
|         5 | Vivek      | Bhati     | 500000 | 2021-06-11 09:00:00 | Admin      |
+-----------+------------+-----------+--------+---------------------+------------+
```

## Q-12. Write an SQL query to print all Worker details from the Worker table order by FIRST_NAME Ascending and DEPARTMENT Descending.

```
Select * from Worker order by FIRST_NAME asc,DEPARTMENT desc;
```
```
+-----------+------------+-----------+--------+---------------------+------------+
| WORKER_ID | FIRST_NAME | LAST_NAME | SALARY | JOINING_DATE        | DEPARTMENT |
+-----------+------------+-----------+--------+---------------------+------------+
|         4 | Amitabh    | Singh     | 500000 | 2021-02-20 09:00:00 | Admin      |
|         8 | Geetika    | Chauhan   |  90000 | 2021-04-11 09:00:00 | Admin      |
|         1 | Monika     | Arora     | 100000 | 2021-02-20 09:00:00 | HR         |
|         2 | Niharika   | Verma     |  80000 | 2021-06-11 09:00:00 | Admin      |
|         7 | Satish     | Kumar     |  75000 | 2021-01-20 09:00:00 | Account    |
|         6 | Vipul      | Diwan     | 200000 | 2021-06-11 09:00:00 | Account    |
|         3 | Vishal     | Singhal   | 300000 | 2021-02-20 09:00:00 | HR         |
|         5 | Vivek      | Bhati     | 500000 | 2021-06-11 09:00:00 | Admin      |
+-----------+------------+-----------+--------+---------------------+------------+
```


## Usage

```python
import foobar


# returns 'words'
foobar.pluralize('word')

# returns 'geese'
foobar.pluralize('goose')

# returns 'phenomenon'
foobar.singularize('phenomena')
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)