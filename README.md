# DataTables

From : https://www.gyrocode.com/articles/jquery-datatables-using-where-join-and-group-by-with-ssp-class-php/


To allow query in server_processing.php $table declaration.


Edit ssp.class.php and replace all instances of FROM `$table` with FROM $table to remove backticks. You will be responsible for escaping your table names if they contain reserved keywords.




From : https://datatables.net/forums/discussion/21242/invalid-json-response-when-adding-some-utf-8-characters


To solve accentuaded charachters problem  with this change in spp.class.php. Only add htmlentitites()


=> blank instead of errors


To get back characters 


I added this line to the function sql_connect() in spp.class.php before returning the $db object and now it works.


$db->exec("set names utf8");

Full modified file ssp.class.php in this repo.
