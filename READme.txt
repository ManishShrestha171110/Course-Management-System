

Database Name: Manish

MariaDB [(none)]> use Manish
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
MariaDB [Manish]> show tables;
+------------------+
| Tables_in_Manish |
+------------------+
| admin            |
| course           |
| pause_course     |
| student          |
| teacher          |
+------------------+
5 rows in set (0.000 sec)

MariaDB [Manish]> desc admin;
+----------+--------------+------+-----+---------+----------------+
| Field    | Type         | Null | Key | Default | Extra          |
+----------+--------------+------+-----+---------+----------------+
| id       | int(11)      | NO   | PRI | NULL    | auto_increment |
| uname    | varchar(100) | YES  |     | NULL    |                |
| password | varchar(100) | YES  |     | NULL    |                |
+----------+--------------+------+-----+---------+----------------+
3 rows in set (0.009 sec)

MariaDB [Manish]> desc course;
+----------+--------------+------+-----+---------+----------------+
| Field    | Type         | Null | Key | Default | Extra          |
+----------+--------------+------+-----+---------+----------------+
| cid      | int(11)      | NO   | PRI | NULL    | auto_increment |
| cname    | varchar(100) | NO   |     | NULL    |                |
| semester | varchar(100) | NO   |     | NULL    |                |
| teacher  | varchar(100) | NO   |     | NULL    |                |
+----------+--------------+------+-----+---------+----------------+
4 rows in set (0.001 sec)

MariaDB [Manish]> desc pause_course;
+-------------+--------------+------+-----+---------+-------+
| Field       | Type         | Null | Key | Default | Extra |
+-------------+--------------+------+-----+---------+-------+
| course_id   | varchar(100) | YES  |     | NULL    |       |
| course_name | varchar(100) | YES  |     | NULL    |       |
| semester    | varchar(100) | YES  |     | NULL    |       |
| teacher     | varchar(100) | YES  |     | NULL    |       |
+-------------+--------------+------+-----+---------+-------+
4 rows in set (0.002 sec)

MariaDB [Manish]> desc student;
+-------------------+--------------+------+-----+---------+----------------+
| Field             | Type         | Null | Key | Default | Extra          |
+-------------------+--------------+------+-----+---------+----------------+
| id                | int(11)      | NO   | PRI | NULL    | auto_increment |
| uname             | varchar(100) | YES  |     | NULL    |                |
| password          | varchar(100) | YES  |     | NULL    |                |
| contact           | int(10)      | YES  |     | NULL    |                |
| semester          | varchar(100) | YES  |     | NULL    |                |
| security_question | varchar(100) | YES  |     | NULL    |                |
| answer            | varchar(100) | YES  |     | NULL    |                |
+-------------------+--------------+------+-----+---------+----------------+
7 rows in set (0.003 sec)

MariaDB [Manish]> desc teacher;
+----------+--------------+------+-----+---------+----------------+
| Field    | Type         | Null | Key | Default | Extra          |
+----------+--------------+------+-----+---------+----------------+
| id       | int(11)      | NO   | PRI | NULL    | auto_increment |
| uname    | varchar(100) | YES  |     | NULL    |                |
| password | varchar(100) | YES  |     | NULL    |                |
| contact  | int(10)      | YES  |     | NULL    |                |
| security | varchar(100) | YES  |     | NULL    |                |
| answer   | varchar(100) | YES  |     | NULL    |                |
+----------+--------------+------+-----+---------+----------------+
6 rows in set (0.005 sec)

// Username and password of Admin.
MariaDB [Manish]> select * from admin;
+----+-------+----------+
| id | uname | password |
+----+-------+----------+
|  1 | admin | 8080     |
+----+-------+----------+
1 row in set (0.008 sec)

