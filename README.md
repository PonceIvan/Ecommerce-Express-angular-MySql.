# Proyectos-stack-MEAN



MRtracker is a web application and android application developed by me
It is like ecommerce application about Pharmacy. in this app there are two types of user one is normal user who can buy online product 
and another is MR(Medical representative) who will deal with doctors about their products and products will be delivered to doctors according to dealing date. MR will be salary based. and location of each MR also be tracked by Admin.
I developed Admin panel Also, in this panel I am maintaing the users, MRs account, order of each MRs, product, location of MRs etc.

I used technologies Angular with typescript,bootstarp,NodeJS,express web server,mysql database 





MRtracker is a web application and android application developed by meIt is like an ecommerce application about Pharmacy. in this app there are two types of user one is a normal user who can buy the online products and another is an MRMedical representative who will deal with doctors about their products and products will be delivered to doctors according to the dealing date. MR will be salary based. and the location of each MR also is tracked by Admin.I developed Admin panel Also, in this panel I am maintaining the users, MRs account, the order of each MRs, product, location of MRs, etc.




describe category;
+-------------+--------------+------+-----+---------+----------------+
| Field       | Type         | Null | Key | Default | Extra          |
+-------------+--------------+------+-----+---------+----------------+
| id          | int(11)      | NO   | PRI | NULL    | auto_increment |
| title       | varchar(200) | YES  |     | NULL    |                |
| formula     | varchar(100) | YES  |     | NULL    |                |
| company     | varchar(50)  | YES  |     | NULL    |                |
| description | varchar(500) | YES  |     | NULL    |                |
+-------------+--------------+------+-----+---------+----------------+


 describe drs;
+-----------+-------------+------+-----+---------+----------------+
| Field     | Type        | Null | Key | Default | Extra          |
+-----------+-------------+------+-----+---------+----------------+
| id        | int(11)     | NO   | PRI | NULL    | auto_increment |
| firstname | varchar(50) | YES  |     | NULL    |                |
| lastname  | varchar(50) | YES  |     | NULL    |                |
| phoneNo   | varchar(50) | YES  |     | NULL    |                |
| degree    | varchar(20) | YES  |     | NULL    |                |
| exist     | int(11)     | YES  |     | NULL    |                |
| MRid      | int(11)     | YES  |     | NULL    |                |
+-----------+-------------+------+-----+---------+----------------+


describe locationofdr;
+---------------------+--------------+------+-----+---------+----------------+
| Field               | Type         | Null | Key | Default | Extra          |
+---------------------+--------------+------+-----+---------+----------------+
| id                  | int(11)      | NO   | PRI | NULL    | auto_increment |
| state               | varchar(100) | YES  |     | NULL    |                |
| city                | varchar(100) | YES  |     | NULL    |                |
| district            | varchar(20)  | YES  |     | NULL    |                |
| pincode             | varchar(10)  | YES  |     | NULL    |                |
| address             | text         | YES  |     | NULL    |                |
| latitude            | varchar(20)  | YES  |     | NULL    |                |
| longitude           | varchar(20)  | YES  |     | NULL    |                |
| drid                | int(11)      | YES  |     | NULL    |                |
| mrid                | int(11)      | YES  |     | NULL    |                |
| fullname            | varchar(50)  | YES  |     | NULL    |                |
| phoneno             | varchar(20)  | YES  |     | NULL    |                |
| orderDetailsTableID | int(11)      | YES  |     | NULL    |                |
+---------------------+--------------+------+-----+---------+----------------+


describe locationofmr;
+-----------+-------------+------+-----+---------+----------------+
| Field     | Type        | Null | Key | Default | Extra          |
+-----------+-------------+------+-----+---------+----------------+
| id        | int(11)     | NO   | PRI | NULL    | auto_increment |
| state     | varchar(10) | YES  |     | NULL    |                |
| city      | varchar(20) | YES  |     | NULL    |                |
| district  | varchar(20) | YES  |     | NULL    |                |
| pincode   | varchar(10) | YES  |     | NULL    |                |
| address   | text        | YES  |     | NULL    |                |
| latitude  | varchar(20) | YES  |     | NULL    |                |
| longitude | varchar(20) | YES  |     | NULL    |                |
| mrid      | int(11)     | YES  |     | NULL    |                |
+-----------+-------------+------+-----+---------+----------------+



 describe mrs;
+-----------+--------------+------+-----+---------+----------------+
| Field     | Type         | Null | Key | Default | Extra          |
+-----------+--------------+------+-----+---------+----------------+
| id        | int(11)      | NO   | PRI | NULL    | auto_increment |
| username  | varchar(50)  | YES  |     | NULL    |                |
| firstname | varchar(50)  | YES  |     | NULL    |                |
| lastname  | varchar(50)  | YES  |     | NULL    |                |
| joindate  | date         | YES  |     | NULL    |                |
| phoneno   | varchar(50)  | YES  |     | NULL    |                |
| email     | varchar(100) | YES  |     | NULL    |                |
| password  | varchar(100) | YES  |     | NULL    |                |
| exist     | int(11)      | YES  |     | NULL    |                |
+-----------+--------------+------+-----+---------+----------------+



describe orderdetails;
+------------------+-----------------------------+------+-----+---------+----------------+
| Field            | Type                        | Null | Key | Default | Extra          |
+------------------+-----------------------------+------+-----+---------+----------------+
| id               | int(11)                     | NO   | PRI | NULL    | auto_increment |
| Quantity         | int(11)                     | YES  |     | NULL    |                |
| OrderDate        | date                        | YES  |     | NULL    |                |
| PayDate          | date                        | YES  |     | NULL    |                |
| totalDiscount    | float                       | YES  |     | NULL    |                |
| totalAmount      | float                       | YES  |     | NULL    |                |
| StatusOfPaymount | enum('Paid','Not Paid')     | YES  |     | NULL    |                |
| PaymentMode      | enum('Cash','Cheque','Upi') | YES  |     | NULL    |                |
| DRid             | int(11)                     | YES  |     | NULL    |                |
| MRid             | int(11)                     | YES  |     | NULL    |                |
| productID        | int(11)                     | YES  |     | NULL    |                |
| flag             | int(11)                     | YES  |     | NULL    |                |
| image            | varchar(200)                | YES  |     | NULL    |                |
| deliveryDate     | date                        | YES  |     | NULL    |                |
| drAddressID      | int(11)                     | YES  |     | NULL    |                |
| addressOFdr      | varchar(200)                | YES  |     | NULL    |                |
| drname           | varchar(50)                 | YES  |     | NULL    |                |
| drphoneno        | varchar(50)                 | YES  |     | NULL    |                |
+------------------+-----------------------------+------+-----+---------+----------------+


describe products;
+-------------------+---------------+------+-----+---------+----------------+
| Field             | Type          | Null | Key | Default | Extra          |
+-------------------+---------------+------+-----+---------+----------------+
| id                | int(11)       | NO   | PRI | NULL    | auto_increment |
| name              | varchar(100)  | YES  |     | NULL    |                |
| price             | float         | YES  |     | NULL    |                |
| discount          | float         | YES  |     | NULL    |                |
| priceWithDiscount | float         | YES  |     | NULL    |                |
| doseInMG          | int(11)       | YES  |     | NULL    |                |
| mgfdate           | date          | YES  |     | NULL    |                |
| expiredate        | date          | YES  |     | NULL    |                |
| description       | varchar(2000) | YES  |     | NULL    |                |
| image             | text          | YES  |     | NULL    |                |
| categoryid        | int(11)       | YES  |     | NULL    |                |
+-------------------+---------------+------+-----+---------+----------------+



describe reportsofmr;
+-----------------+---------+------+-----+---------+----------------+
| Field           | Type    | Null | Key | Default | Extra          |
+-----------------+---------+------+-----+---------+----------------+
| id              | int(11) | NO   | PRI | NULL    | auto_increment |
| noOfOrders      | int(11) | YES  |     | NULL    |                |
| salaryPerDeal   | float   | YES  |     | NULL    |                |
| noOfDeals       | int(11) | YES  |     | NULL    |                |
| totolMakeAmount | float   | YES  |     | NULL    |                |
| MRid            | int(11) | YES  |     | NULL    |                |
+-----------------+---------+------+-----+---------+----------------+


