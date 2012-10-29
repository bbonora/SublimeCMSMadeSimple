SublimeCMSMadeSimple
====================
Sublime Text 2 CMS Made Simple package is a collection of CMS Made Simple snippets and autocompletions for Sublime Text 2. It includes all of the methods found in the CMSModule class plus a few commonly used snippets for PHP and smarty programing.

Installation
------------
Install the pacakge via the package countrol (CMS Made Simple) or clone the contents of the repo in your Sublime Text 2 package directory.

Usage
-----
**PHP Files:** Begin typing the name of the method you would like to use. The autocompletion menu will appear. Select the desired function from the list. Most all methods have placeholders. You can cycle through the placeholders using the tab key. A list of all the available CMSModule class methods can be viewed here:
+ http://apidoc.cmsmadesimple.org/CMS/CMSModule.html

**Smarty Files (*.tpl):** Type the full name of the snippet followed by the tab key.

Available Snippets
------------------
###PHP
+ **cms_db** - `$db = cmsms()->GetDb();`
+ **cms_dict** - `$dict = NewDataDictionary($db);`
+ **cms_loop** - 
```
while($results && $row = $results->FetchRow())
{
	$onerow = stdClass;
	$onerow->name = $row['name'];
	
	$entryarray[] = $onerow;
}
```

###Smarty
+ **smarty_foreach** - ``

Author
------
**Ben Bonora**
+ http://twitter.com/bbonora
+ http://github.com/bbonora
+ http://www.bennyvbonora.com

