- Durgesh sir class 
	- DBMS
		- .DB file : consist of multiple 
- When working with a tech company or a team start and stop database is not required, as the database is already start (open) on the servers.

- connect hr 
	- then enter password
- set autocommit on
	- Set's commit to happen in every 5 secs
- connect system
	- Enter password 
	- Connected shows up 
- create user temp identified by 123456;
	- Temp is the name of your user 
	- 123456 is password for user temp 
- connect temp
	- Enter password 
	- Error : user TEMP lacks CREATE SESSION privilage; logon denied
- connect system
	- Enter password
- grant resource, connect to temp;
	- If we add ,dba user becomes admin
- connect temp
	- Account lock error can happen 
	- To fix alter user account unlock 

- 3 level in dbs
	- View level
	- Logical level
	- Physical level 

- Trigger can be used to make copy bcz it does not require a socket for copying
	- Trigger is :
		- Create trigger 'name' afterinsert begin {
			insert into table values (101,....)-
			}


- Truncate and delete is same but delete works from log so it can be rolled back while, truncate can not be rolled back 
- 