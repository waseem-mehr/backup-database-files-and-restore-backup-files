# backup-database-files-and-restore-backup-files
if you are using sqlLite database and want to shift postgresql database but there <br>
is data in sqlLite database and you dont want to lose this data so the solution is <br>
first of all create backup of this database my using run the command given below <br>
<b>python manage.py dumpdata > datadump.json </b>
this will create a json file with all the tables and records of the data and then <br>
delete the sqlLite database and change the database settings in setting.py file <br>
add postgresql database and credentials and the run the commands <br>
<b>python manage.py makemigrations</b> 
<b>python manage.py migrate or python manage.py --run-syncbd</b>
after this store the backup that created by us by using the following command
<b>python manage.py loaddata dumpdata.json </b>
that it.Happy Coding :) 
