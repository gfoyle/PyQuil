You need to provide protocol and query string for the conn string to work

### sqlite
sqlite:///test.db

### mssql
mssql+pyodbc:///DRIVER={FreeTDS};SERVERNAME=orchid;UID=sa;PWD=pwd;DATABASE=db'
 - Driver is defined in odbcinst.ini 
 - servername is defined freetds.conf 

If you are on windows use DRIVER={SQL SERVER} instead.

MSSQL driver does not support "SELECT \*", you must provide the columns you want.

### Postgres:
postgresql+psycopg2://user:password@host:port/dbname

### All others:
http://www.sqlalchemy.org/docs/dialects/