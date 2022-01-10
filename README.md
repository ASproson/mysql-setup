# mysql-setup

## MySQL Download & Install

[Initial YouTube Guide](https://www.youtube.com/watch?v=2_j_zufGdX4&ab_channel=BoostMyTool)

1. MySQL website, download mysql-installer-community
2. Custom install
3. Expand MySQL Workbench > MySQL WorkBench 8.0, transfer to Products To Be Installed
4. Expand MySQL Server > MySQL Server 8.0, trans to Products To Be Installed
5. Set Root Password
6. Leave Windows Service as default
7. Execute until installation Complete
8. Untick Start MySQL Workbench after setup
9. Navigate to C/Program Files/MySQL/MySQL Server 8.0/bin, copy file path
10. Windows key, search 'advanced settings'
11. Environment Variables
12. Click Path, edit, New
13. Paste in file path, hit ok until all windows cleared
14. Windows key, search 'command prompt'
15. mysql --version
16. mysql -u root -p
17. SHOW DATABASES;

## Connect MySQL to VSCode

[Initial YouTube Guide 2](https://www.youtube.com/watch?v=wzdCpJY6Y4c&ab_channel=BoostMyTool)

1. Extensions > [SQLTools](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools) by Matheus Teixeira
2. Extensions > @tag:sqltools-driver [SQL Tools MySQL/MariaDB](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools-driver-mysql)
3. Connection assistant > MySQL
4. Connection Name: FirstMySQLInstance
5. Database: testdb
6. Save password
7. Test Connection, Save Connection
8. ER_NOT_SUPPORTED_AUTH_MODE > Need to use an older access method
9. Windows key, search 'command prompt'
10. mysql -u root -p
11. CREATE USER 'sqluser'@'%' IDENTIFIED WITH mysql_native_password BY 'password';
12. GRANT ALL PRIVILEGES ON *.* TO 'sqluser'@'%';
13. FLUSH PRIVILEGES;
14. Disconnect the connection to the DB using the connection icon in VSCode
15. Change username to sqluser
16. Change password to password
17. CREATE DATABASE testdb;
18. Doesn't appear? Right click on connection, refresh, or disconnect and reconnect, it now appears
