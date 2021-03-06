======
Tables
======

In format 2, the following column names are interpreted

- variable
- scenario
- type
- ref value
- param
- initial_value_proportional_variation
- unit
- mean growth
- variability growth
- ref date
- label
- comment
- source

Example
-------


+----------+----------+--------+-------------------------------------------------------+--------+--------------------------------------+------+-------------+--------------------+------------+------------+---------+--------+
| variable | scenario | type   | ref value                                             | param  | initial_value_proportional_variation | unit | mean growth | variability growth | ref date   | label      | comment | source |
+----------+----------+--------+-------------------------------------------------------+--------+--------------------------------------+------+-------------+--------------------+------------+------------+---------+--------+
| a        |          | exp    | 10                                                    |        | 0.4                                  | kg   | -0.20       | 0.10               | 01/01/2009 | test var 1 |         |        |
+----------+----------+--------+-------------------------------------------------------+--------+--------------------------------------+------+-------------+--------------------+------------+------------+---------+--------+
| b        |          | interp | {"2010-01-01":1, "2010-03-01":100 , "2010-12-01":110} | linear | 0.4                                  | kg   | -0.20       | 0.10               | 01/01/2009 | test var 1 |         |        |
+----------+----------+--------+-------------------------------------------------------+--------+--------------------------------------+------+-------------+--------------------+------------+------------+---------+--------+


Format v1
==========
This format does not allow to specify growth of uncertainty over time.

- variable
- scenario
- module
- distribution
- param 1
- param 2
- param 3
- unit
- start date
- end date
- CAGR
- ref date
- label
- comment
- source

Example
-------
+----------+----------+--------------+--------------+---------+---------+---------+------+------------+------------+------+------------+------------+---------+--------+
| variable | scenario | module       | distribution | param 1 | param 2 | param 3 | unit | start date | end date   | CAGR | ref date   | label      | comment | source |
+----------+----------+--------------+--------------+---------+---------+---------+------+------------+------------+------+------------+------------+---------+--------+
| z        |          | numpy.random | choice       | 1       | 2       |         | kg   | 01/01/2009 | 01/04/2009 | 0.10 | 01/01/2009 | test var 1 |         |        |
+----------+----------+--------------+--------------+---------+---------+---------+------+------------+------------+------+------------+------------+---------+--------+
