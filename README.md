# php-snmp


##Automatically exported from code.google.com/p/php-snmp

### Original informations
Code license: GNU GPL v3

Author: T.Kalapun

### Original home page
**NOTE
Right now due to many work I don't have much time to make changes and fix bugs. If some-one wants to, mail me and I'll give you access to sources**

This class is for sending SNMP v2c traps from directly PHP, without using any command-line utilites or modules. Just socket_open and socket_sendto

**Usage:**
```php
<?php

$host = '192.168.1.1';
$community = 'public';

$vars[] = array(
    'oid'    => '1.3.6.1.4.1.143.101.14.1.1.2.0',
    'value' => 'message 1'
    );
$vars[] = array(
    'oid'    => '1.3.6.1.4.1.143.101.14.1.1.2.1', 
    'value' => 'message 2',
    'type'   => 's'
    ); 

SNMP::trap($host, $vars, $community);
?>
```
