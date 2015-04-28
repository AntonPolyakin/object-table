Display JSON in Table with AngularJS
=================

Code licensed under MIT license.

This directive allow show your data in tables. It support searching, filtering and pagination.
Hight perfomance. Sorting one or more fields!


## Installing via Bower
```
bower install angular-object-table
```

## Using

```
<link rel="stylesheet" type="text/css" href="{path to library}/build/object-table-style.css">

<script type="text/javascript" src="{path to library}/build/object-table.js"></script>

<!-- optional -->
<link rel="stylesheet" type="text/css" href="http://getbootstrap.com/dist/css/bootstrap.min.css">
```
Add dependency:
```
angular.module('yourModule', ['objectTable'])
```

Add HTML-markup :
```
<table object-table 
       from-url="http://some-url.com/getData" 
       data="exportDataVariable" 
       display="2" 
       headers="Name, Age" 
       fields="name, age"
       sorting="false"
></table>
```

## Atributes

Here is a file list for possible attributes for stable version:

Atribute             | Description
---------------------|----------------
data                 | *required* - data source (array of objects) in your Controller. But if 'fromUrl' is present 'data' atribute will contain controller link to empty array( will be fill up after receiving data ).
fromUrl				 | - load data from external URL. 
display     		 | *default: 5* - Display count. Using with pagging is displayed items per page
search               | *default: true* - Display search input 
pagging				 | *default: true* - Use pagging to present data
headers              | *required* - Example: ['HeaderName1','HeaderName2']. - Array of table header names
fields  			 | *required* - Example: ['property1','property2'].  - Array of displayed properties of object. This option allows you to display only certain fields of the object. Number of fields must be equal number of headers.
sorting				 | *default: simple*. Use sorting feature. 'simple' - by single column. 'compound' - order by multiple fields.
