Login panel is a very common things in every Project,So if we learn it completely then it help us a lot in future.

I hope all of you easily made that kind of UI, But remember that for make a login panel you need a Forms Tag ,in Form Tag A attribute named [ action=“your.php” ]

it means Action tag sent your data with Get/post method with your selected Php page.

For login here we use isadmin.php page and for Registration we use reg_Confirm.php page.

First we demonstrate isadmin.php page.

First Session :

We just write the information about our data base:

$host=”localhost”;   
$username=”root”;
$password=””;
$db_name=”cow_hunt”;
$tbl_name=”usertable”;

5 global variable we use here to store the information.

 

Second session we use for connect to the database using MySqli

mysql_connect(“$host”, “$username”, “$password”)or die(“cannot connect”);
mysql_select_db(“$db_name”)or die(“cannot select DB”);

 

Third Session we just receive post data from previous string

 

$myusername=$_POST[‘name’];
$mypassword=$_POST[‘password’];

 

Fourth session we knoct the database and get all the data from selected table and check them with our receiving data,and record the result it match or not.

$sql=”SELECT * FROM $tbl_name WHERE UserEmail=’$myusername’ and UserPassword=’$mypassword'”;
$result=mysql_query($sql);
$count=mysql_num_rows($result);

 

Fifth session we just print if match or not, if match we output Hello Admin,and if not then Wrong Username or Password.

 

If you understand the full idea then you easily make your own login panel.

Here i share the Demo code and the Sql file,and also upload the script with our workshop server.


Live Demo : http://fnfbd.org/workshop/demo/login.php