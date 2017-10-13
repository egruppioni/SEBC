```
[root@ip-172-31-15-151 yum.repos.d]# /usr/share/cmf/schema/scm_prepare_database.                                                                                                                               sh mysql -h ip-172-31-4-206 -uroot -p --scm-host ip-172-31-15-151 scm scm scm  -                                                                                                                               -force
Enter database password:
JAVA_HOME=/usr/lib/jvm/jre-openjdk
Verifying that we can write to /etc/cloudera-scm-server
[                          main] DbProvisioner                  ERROR Exception                                                                                                                                when creating/dropping database with user 'root' and jdbc url 'jdbc:mysql://ip-1                                                                                                                               72-31-4-206/?useUnicode=true&characterEncoding=UTF-8'
java.sql.SQLException: Can't create database 'scm'; database exists
        at com.mysql.jdbc.SQLError.createSQLException(SQLError.java:1073)[mysql-                                                                                                                               connector-java-5.1.17.jar:]
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3597)[mysql-conn                                                                                                                               ector-java-5.1.17.jar:]
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3529)[mysql-conn                                                                                                                               ector-java-5.1.17.jar:]
        at com.mysql.jdbc.MysqlIO.sendCommand(MysqlIO.java:1990)[mysql-connector                                                                                                                               -java-5.1.17.jar:]
        at com.mysql.jdbc.MysqlIO.sqlQueryDirect(MysqlIO.java:2151)[mysql-connec                                                                                                                               tor-java-5.1.17.jar:]
        at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2619)[mysql                                                                                                                               -connector-java-5.1.17.jar:]
        at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2569)[mysql                                                                                                                               -connector-java-5.1.17.jar:]
        at com.mysql.jdbc.StatementImpl.execute(StatementImpl.java:824)[mysql-co                                                                                                                               nnector-java-5.1.17.jar:]
        at com.mysql.jdbc.StatementImpl.execute(StatementImpl.java:667)[mysql-co                                                                                                                               nnector-java-5.1.17.jar:]
        at com.cloudera.enterprise.dbutil.DbProvisioner.executeSql(DbProvisioner                                                                                                                               .java:299)[db-common-5.13.0.jar:]
        at com.cloudera.enterprise.dbutil.DbProvisioner.doMain(DbProvisioner.jav                                                                                                                               a:104)[db-common-5.13.0.jar:]
        at com.cloudera.enterprise.dbutil.DbProvisioner.main(DbProvisioner.java:                                                                                                                               123)[db-common-5.13.0.jar:]
[                          main] DbProvisioner                  ERROR Stack Trac                                                                                                                               e:
java.sql.SQLException: Can't create database 'scm'; database exists
        at com.mysql.jdbc.SQLError.createSQLException(SQLError.java:1073)[mysql-                                                                                                                               connector-java-5.1.17.jar:]
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3597)[mysql-conn                                                                                                                               ector-java-5.1.17.jar:]
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3529)[mysql-conn                                                                                                                               ector-java-5.1.17.jar:]
        at com.mysql.jdbc.MysqlIO.sendCommand(MysqlIO.java:1990)[mysql-connector                                                                                                                               -java-5.1.17.jar:]
        at com.mysql.jdbc.MysqlIO.sqlQueryDirect(MysqlIO.java:2151)[mysql-connec                                                                                                                               tor-java-5.1.17.jar:]
        at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2619)[mysql                                                                                                                               -connector-java-5.1.17.jar:]
        at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2569)[mysql                                                                                                                               -connector-java-5.1.17.jar:]
        at com.mysql.jdbc.StatementImpl.execute(StatementImpl.java:824)[mysql-co                                                                                                                               nnector-java-5.1.17.jar:]
        at com.mysql.jdbc.StatementImpl.execute(StatementImpl.java:667)[mysql-co                                                                                                                               nnector-java-5.1.17.jar:]
        at com.cloudera.enterprise.dbutil.DbProvisioner.executeSql(DbProvisioner                                                                                                                               .java:299)[db-common-5.13.0.jar:]
        at com.cloudera.enterprise.dbutil.DbProvisioner.doMain(DbProvisioner.jav                                                                                                                               a:104)[db-common-5.13.0.jar:]
        at com.cloudera.enterprise.dbutil.DbProvisioner.main(DbProvisioner.java:                                                                                                                               123)[db-common-5.13.0.jar:]
--> Error 1, ignoring (because force flag is set)
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/lib/jvm/jre-openjdk/bin/java -cp /usr/share/java/mysql-connecto                                                                                                                               r-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../li                                                                                                                               b/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db                                                                                                                               .properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Unable to                                                                                                                                login using supplied username/password.
[                          main] DbCommandExecutor              ERROR Error when                                                                                                                                connecting to database.
java.sql.SQLException: Access denied for user 'scm'@'ip-172-31-15-151.eu-central                                                                                                                               -1.compute.internal' (using password: YES)
        at com.mysql.jdbc.SQLError.createSQLException(SQLError.java:1073)[mysql-                                                                                                                               connector-java-5.1.17.jar:]
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3597)[mysql-conn                                                                                                                               ector-java-5.1.17.jar:]
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3529)[mysql-conn                                                                                                                               ector-java-5.1.17.jar:]
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:935)[mysql-conne                                                                                                                               ctor-java-5.1.17.jar:]
        at com.mysql.jdbc.MysqlIO.secureAuth411(MysqlIO.java:4101)[mysql-connect                                                                                                                               or-java-5.1.17.jar:]
        at com.mysql.jdbc.MysqlIO.doHandshake(MysqlIO.java:1300)[mysql-connector                                                                                                                               -java-5.1.17.jar:]
        at com.mysql.jdbc.ConnectionImpl.coreConnect(ConnectionImpl.java:2337)[m                                                                                                                               ysql-connector-java-5.1.17.jar:]
        at com.mysql.jdbc.ConnectionImpl.connectOneTryOnly(ConnectionImpl.java:2                                                                                                                               370)[mysql-connector-java-5.1.17.jar:]
        at com.mysql.jdbc.ConnectionImpl.createNewIO(ConnectionImpl.java:2154)[m                                                                                                                               ysql-connector-java-5.1.17.jar:]
        at com.mysql.jdbc.ConnectionImpl.<init>(ConnectionImpl.java:792)[mysql-c                                                                                                                               onnector-java-5.1.17.jar:]
        at com.mysql.jdbc.JDBC4Connection.<init>(JDBC4Connection.java:49)[mysql-                                                                                                                               connector-java-5.1.17.jar:]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method)                                                                                                                               [:1.8.0_144]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstruct                                                                                                                               orAccessorImpl.java:62)[:1.8.0_144]
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingC                                                                                                                               onstructorAccessorImpl.java:45)[:1.8.0_144]
        at java.lang.reflect.Constructor.newInstance(Constructor.java:423)[:1.8.                                                                                                                               0_144]
        at com.mysql.jdbc.Util.handleNewInstance(Util.java:411)[mysql-connector-                                                                                                                               java-5.1.17.jar:]
        at com.mysql.jdbc.ConnectionImpl.getInstance(ConnectionImpl.java:381)[my                                                                                                                               sql-connector-java-5.1.17.jar:]
        at com.mysql.jdbc.NonRegisteringDriver.connect(NonRegisteringDriver.java                                                                                                                               :305)[mysql-connector-java-5.1.17.jar:]
        at java.sql.DriverManager.getConnection(DriverManager.java:664)[:1.8.0_1                                                                                                                               44]
        at java.sql.DriverManager.getConnection(DriverManager.java:247)[:1.8.0_1                                                                                                                               44]
        at com.cloudera.enterprise.dbutil.DbCommandExecutor.testDbConnection(DbC                                                                                                                               ommandExecutor.java:253)[db-common-5.13.0.jar:]
        at com.cloudera.enterprise.dbutil.DbCommandExecutor.main(DbCommandExecut                                                                                                                               or.java:138)[db-common-5.13.0.jar:]
[                          main] DbCommandExecutor              ERROR Exiting wi                                                                                                                               th exit code 8
--> Error 8, ignoring (because force flag is set)
All done, your SCM database is configured correctly!



```


```

[root@ip-172-31-15-151 yum.repos.d]# cat /etc/cloudera-scm-server/db.properties
# Auto-generated by scm_prepare_database.sh on Fri Oct 13 03:47:32 EDT 2017
#
# For information describing how to configure the Cloudera Manager Server
# to connect to databases, see the "Cloudera Manager Installation Guide."
#
com.cloudera.cmf.db.type=mysql
com.cloudera.cmf.db.host=ip-172-31-4-206
com.cloudera.cmf.db.name=scm
com.cloudera.cmf.db.user=scm
com.cloudera.cmf.db.setupType=EXTERNAL
com.cloudera.cmf.db.password=scm


```