# How to create MySQL DB using AWS RDS (free service)

<br>

### Prerequisites
  - AWS account

<br>

## Create database

   - Login to AWS Console
   - It should display the AWS Management Console Dashboard.
   - Type in the searchfield `Find Services`: ``` rds ```
   - hit `Enter`.

It will redirect to RDS Dashboard, you should see `Amazon RDS` on the left.

<br>

**1. RDS Dashboard**

If this is the first time to create database, you can just hit button `Create database`...

<img src="assets/aws-rds-create.png">


...or go to menupoint: `Databases` and find button `Create database` in the top right corner.

<br>

**2. Select engine**

Now you should see the databases listed in squares.

   - Check if you are using free service.
   <img src="assets/aws-rds-free-use.png">

   - Select MySQL.
   - Hit `Next`.

<br>

**3. Specify DB details**

you should see something like this:

<img src="assets/aws-specify.db-details.png">

if you need more specified settings, you can select and set them.

<br>

Scroll down for "Settings pane" and set: 

 - DB instance identifier
 - Master username
 - Master password (requires confirmation)

...hit button `Next`.

<br>

**4. Configure advanced settings**

* **Network & Security**

Use default values and make sure it is set to public.

<img src="assets/aws-conf-advance-set.png">

<br>

* **Database options**

Set name, port of your database...

**...the rest of the settings can be left as default.**

Hit button `Create database` on the bottom of the page.

Upon success, you should see something like this:

<img src="assets/aws-rds-db-success.png">

<br>

**Now your database has been created**

<br>


## Connect to DB via terminal

Open a terminal.

Type:

```
$ mysql -h mysql–test-instance1.123456789012.us-east-1.rds.amazonaws.com -P 3306 -u mymasteruser -p
```

explained...

```
$ mysql -h <url> -P <port> -u <user> -p
```


if succeded, you should see:

```
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 350
Server version: 5.6.40-log MySQL Community Server (GPL)

Type 'help;' or '\h' for help. Type '\c' to clear the buffer.

mysql>
```

You are now able to use sql commands.

For more info and detailed explanation, visit [this site](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ConnectToInstance.html) .

