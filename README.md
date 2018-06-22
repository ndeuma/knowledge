# 2018
## June
### 2018-06-21
[In Chrome Developer Tools, you can set multiple breakpoints per line](https://umaar.com/dev-tips/129-inline-breakpoints/)

# 2017
## December
### 2017-12-20
When you cannot execute images/appliances in VirtualBox, and the error message is "VT-x is not active" despite being enabled in the BIOS, the Hyper-V service in Windows has to be deleted:

`  dism.exe /Online /Disable-Feature:Microsoft-Hyper-V`

### 2017-12-08
Quickly create a 100 MB file for testing with large files:

`  dd if=/dev/zero of=100M.dat bs=1kB count=99999`

## October
### 2017-10-20
When mysqldump fails with the error message

`  mysqldump: [ERROR] unknown variable 'set-variable=max_allowed_packet=100M'`

on the command line, the parameter `--defaults-file` has to be set:

`  mysqldump --defaults-file=C:\MySQL\my.ini -uusername -ppassword databasename >Dump.sql`

## September
### 2017-09-06
Search for a class or package name in \*.jar files:

`    for file in *.jar; do echo "========== ${file} =========="; jar tf $file | grep foo; done`

### 2017-09-01
How to fetch the latest version of a file in Git without using `git pull`

`   git fetch origin <branch>`

`   git checkout FETCH_HEAD -- <file>`

## August
### 2017-08-17

How to configure logging in tomcat.log for a Tomcat-based web application: Put

`   org.apache.level = ALL`

in `logging.properties`. This creates huge amounts of log data, but you can narrow it down to HTTP connections, for example:

`   org.apache.coyote.level = FINE`

## July
### 2017-07-21
Directories that cannot be deleted in Windows Explorer due to too long path names can be deleted in Git Bash using `rm -Rf`

## May
### 2017-05-17
A column that is case insensitive can be queried in a case sensitive way using the keyword `binary` in MySQL:

`  select bar from foo where binary bar = 'qux'`

## February
### 2017-02-23
How to temporarily disable foreign key constraint checks in MySQL:

`  set foreign_key_checks = 0;`

`  // Delete stuff`

`  set foreign_key_checks = 1;`

## January
### 2017-01-23
[Very good article on HTTPS configuration in Tomcat](https://blog.eveoh.nl/2014/02/tls-ssl-ciphers-pfs-tomcat/)

# 2016

## November
### 2016-11-04
[Eclipse-based applications and antivirus software](http://weaklyreachable.blogspot.de/2014/04/eclipse-osgi-windows-virus.html)

## October
### 2016-10-19
[Migrating legacy OSGi applications to Java 8](http://stackoverflow.com/questions/24669940/java-8-missing-required-capability-require-capability-osgi-ee-filter-osg)

## June
### 2016-06-22
Search for files with a given name and copy all found files into some directory, including the folder structure:

`  find . -name '*SE_V6*.jsp' | xargs cp --parents -t /C/Users/Peter/Temp/`

## May
### 2016-05-17
In Balsamiq, you have to write "\_F" instead of "F" when creating tree widget entries starting with "F", because "F" is the "folder" icon.

## March
## 2016-03-01
[The most common OpenSSL commands](https://www.sslshopper.com/article-most-common-openssl-commands.html)
