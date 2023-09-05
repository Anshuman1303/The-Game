# The-Game
This "game" was created by my team and me for our CBSE class 12 project. It has a sophisticated login and admin system. This is merely a proof of concept, as I haven't used a central database.
Run the following commands in mysql command line to make the script work.  
```create database gamedb;```  
```use gamedb;```  
```create table userdb(username varchar(20) primary key, password varchar(100) not null, money float not null, admin varchar(1) default 'F', banned date default NULL);```  
```create table usermsgs(sender varchar(20) not null,recipient varchar(20) not null, message varchar(1024) not null, IsRead varchar(1) default 'F', MsgTimeStamp datetime default```   
```current_timestamp, foreign key (sender) references userdb (username),foreign key (recipient) references userdb (username));```  
```insert into userdb values('admin','admin123',1.175494351E+38,'T',null);```  
Also enter you password in ```MYSQLPASSWORD``` available at the top of the python file. If any other credentials need changing do so appropriately
Also, make sure you have the following packages installed
pymysql
random
datetime
