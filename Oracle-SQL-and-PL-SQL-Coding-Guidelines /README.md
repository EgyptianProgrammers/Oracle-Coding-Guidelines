# **Oracle SQL and PL/SQL Coding Guidelines**

The main purpose of **Oracle SQL and PL/SQL Coding Guidelines** to define the standards and guidelines for Oracle PL/SQL developers. These guidelines will be maintained and reviewed frequently to improve it and reach the best practices to write, maintain and enhancement the Oracle SQL and Pl/SQL. It was created by Egyptian Programmers.

 ## Oracle SQL and PL/SQL Coding Guidelines
 
1. **Introduction**
     - Overview
2. **Naming Conventions**
     - Oracle Database Objects
     - Oracle PL/SQL Objects
     - File Extensions

</br>

## Introduction

The main purpose of Oracle SQL and PL/SQL Coding Guidelines to define the standards and guidelines for Oracle PL/SQL developers. this guideline will be maintained and reviewed frequently to improve it and reach the best practices to write, maintain and enhancement the Oracle SQL and Pl/SQL code.

**Naming Convention** In computer programming, a naming convention is a set of rules for choosing the character sequence to be used for identifiers which denote variables, types, functions, and other entities in source code and documentation.
</br>
<b>Reference: </b><a href="https://en.wikipedia.org/wiki/Naming_convention_(programming)"> wikipedia</a>

</br>

## Naming Conventions
This is the Egyptian programmers naming conventions for Oracle database objects and PL/SQL code.

### Oracle Database Objects
This is the standard of oracle database objects
<br>
##### Syntax 

> **[optional {module_abbr}{separator}]{prefix}{separator}{identifier_name}{separator}{suffix}**

 | SEQ       | Object Name               | Length | Prefix | Suffix | Example |
 | :-        | :----                     | :-:    | :---   | :---   | :----   |
 | 1         | **Tables**                    | -     |  -      |  -      | -|
 | 1         | Table                    | 30     |        |        | customers, customer_headers and pos_customer_headers |
 | 1         | Temporary Table           | 30     |        | _tmp   |customers_update_tmp|
 | 1.1       | **Table Constraints**        | -      |    -   |  -     |   -      |
 | 1.1.1     | Primary Key               |        |        | _pk    | customer_id_pk | 
 | 1.1.2     | Foreign Key               |        |        | _fk    | customer_id_fk |
 | 1.1.3     | Check Key                 |        |        | _ck    | customer_mobile_ck | 
 | 1.1.4     | Unique Key                |        |        | _uk    | customer_mobile_uk | 
 |1.1.5      | Index                     | 30     |        | _idx   | customer_id_idx |
 | 2         | Views                     | 30     |        | _v     | customers_v, customer_headers_v and pos_customer_headers_v |
 | 3         | Materialized Views        | 30     |        |  _mv   |customers_mv, customer_headers_mv and pos_customer_headers_mv |
 | 4         | **Packages**                  |  -     | -      |   -    |   -    |-|
 | 4.1       | Packages: Table Handlers  | 30     |        | _pkg   | customer_headers_pkg |
 | 4.1.1     | Insert Procedures         | 30     |ins_    |        | ins_customer  |
 | 4.1.2     | Update Procedures         | 30     |upd_    |        | upd_customer |
 | 4.1.3     | Delete Procedures         | 30     |del_    |        | del_customer |
 | 4.2       | Public Packages           | 30     |        | _api   | customer_headers_api |
 | 4.3       | Private Packages          | 30     |        | _pvt   | customer_headers_pvt |
 | 4.4       | Wrapped Packages          | 30     |        | _wrap  | customer_headers_wrap |
 | 4.5       | Procedures                | 30     |        |        | transfer_customer |
 | 4.6       | Functions                 | 30     |        |        | get_customer_name |
 | 5         | Standalone Procedures     | 30     |        |        | transfer_customer_proc |
 | 6         | Standalone Functions      | 30     |        |        | get_customer_name_func |
 | 7         | Sequences                 | 30     |        | _seq   | customer_id_seq |
 | 8         | Synonyms                  | 30     |        |        |                 |
 | 9         | Triggers                  | 30     |        | _trg   | concate_cutomer_name_trg | 
 | 10        | Directories               | 30     |        | _dir   | customer_accounts_dir |
 | 11        | Context                   | 30     |        | _con   | customer_accounts_con | 
 | 12        | Collection Types          | -      |        | -      | -        | 
 | 12.1      | Arrays                    |        | r_     | _type  | r_customer_type | 
 | 12.2      | Tables                    |        | t_     | _type  | t_customer_type |  
 | 12.3      | Objects                   |        | o_     | _type  | o_customer_type |  
 
</br>
Notes: **pos** is abbreviation or short for **P**oint **O**f **S**ale, and we will use it as module abbreviation for example.

</br>
 
### Oracle PL/SQL Objects
This is the standard of oracle PL/SQL objects.
##### Syntax 

> **{scope}{prefix}{separator}{identifier_name}{separator}{suffix}**

 | SEQ | Object Name                | Length | scope | Prefix | Suffix | Example           |
 | :-  | :----                      | :-:    | :--   | :---   | :--    | :----             |
 | 1   | **Variables**                  |        |       |       |        |                  |
 | 1.1 | Global Variable            |        | g     |    _    |        | g_enterprise_id   | 
 | 1.2 | Local Variable             |        | l     |    _    |        | l_customer_id     | 
 | 2   | **Constants**                  |        |       |       |       |                  |
 | 2.1 | Global Constants           |        | g     |  c     |        | gc_max_discount   | 
 | 2.2 | Local Constants            |        | l     |  c     |        | lc_max_discount   | 
 | 3   | **Parameters**                 |  -     |       |  -     |  -     |    -              |
 | 3.1 | Cursor Parameters          |        |       | p      |        | p_customer        |
 | 3.2 | In Parameters              |        |       | p      |        | p_customer_id     | 
 | 3.3 | Out Parameters             |        |       | x      |        | x_customer_id     | 
 | 3.4 | In/Out Parameters          |        |       | px     |        | xp_customer_id    | 
 | 4   | **Other Objects Definitions**  |    -   |       |   -    |   -    |     -             | 
 | 4.1 | Cursors                    |        |       | cur    |        | cur_customers     |
 | 4.2 | Record                     |        |       | r      |  type  | r_customer_type   | 
 | 4.3 | Array / Table              |        |       | t      |  type  | t_customers_type  |    
 | 4.4 | Objects                    |        |       | o      |  type  | o_customers_type  |
 | 4.5 | Exceptions                 |        |       | e      |        | e_customer_exists |
 | 4.6 | Exception Number           |        |       | en     |        | en_customer_exists|
 
</br> </br>
<h2>File Extensions</h2>

 | SEQ | Object Name           | Extension | Example                  | Remarks   |
 | :-: | :---                  | :---      | :---                     | :-------- |
 | 1   |     **Package**    |
 | 1.1 | Package Specification | .pks      | customer_headers_api.pks |           |
 | 1.2 | Package Body          | .pkb      | customer_headers_api.pkb |           |
 | 2   | Everything else       | .sql      | customer_headers.sql     |           |   


</br>

## Appendix
The appendix section that presents elements syntax and describes it.

 | SEQ | Element Syntax    | Element Name.       | Description |
 | :-: | :---              | :--                 | :--------   |
 | 1   | {separator}       | Separator           |             |  
 | 2   | {scope}           | Scope               |             |  
 | 3   | {identifier_name} | Identifier Name     |             | 
 | 4   | {module_name}     | Module* Name        |             |
 | 5   | {module_abbr}     | Module Name         |             |
 | 6   | {table_name}      | Table Name          |             |
 | 7   | {table_abbr}      | Table Abbreviation  |             |
 | 8   | {column_name}     | Column Name         |             |
 | 9   | {column_abbr}     | Column Abbreviation |             |

</br>

## Contributing to the guidelines
We welcome new Oracle developers to join our community and contribute to the Oracle coding guidelines project. If you are interested in helping please don’t hesitate to contact on an e-mail: info@egyptianprogrammers.com

</br>

###### Suggestions & Issues
> If you find any issue or have a great idea in mind please create an issue on <a href="https://github.com/EgyptianProgrammers/Oracle-Coding-Guidelines/issues">GitHub</a>.
