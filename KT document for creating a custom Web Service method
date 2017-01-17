
Team         : EMR Team.

	To create a custom WebService method, there are three things to be done
i.	Register a custom WebService method
ii.	Define code of custom WebService method
iii.	Define return fields of custom WebService method

Below is the Step wise Process Flow of :

Steps to register a custom WebService method:

●	Every WS method should be registered before its code is defined. The registration is defining a register array that has WS method name, its input parameters’ name and type array and its return value.
●	The below given is a register array  of a custom WS method named look_up_value.

$server->register(
     	'look_up_value',
   	  array(
'session'=>'xsd:string', 'module_name'=>'xsd:string', 'field'=>'xsd:string', 'value'=>'xsd:string',  'deleted'=>'xsd:int'),
     	array('return'=>'tns:look_up_value_count'),
	$NAMESPACE);

●	Above register array should be defined just above the definition of 'look_up_value' method at location <root>/soap/SoapSugarUsers.php file.

Steps to define code of custom WebService method:

●	Custom WS method should be defined along with default WS methods defined in <root>/soap/SoapSugarUsers.php file
●	Defining a custom WS method is like defining any other method that implements a logic and returns an array of values as per the requirement.
●	Following is code defined in look_up_value method that returns count of number of times a user input value exists in given module in a given field

function look_up_value($session, $module_name, $field, $value){
	global  $beanList, $beanFiles;
   	 $error = new SoapError();
