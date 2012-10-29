SublimeCMSMadeSimple
====================
Sublime Text 2 CMS Made Simple package is a collection of CMS Made Simple snippets and auto-completions for Sublime Text 2. It includes all of the methods found in the CMSModule class plus a few commonly used snippets for PHP and smarty programing.

Installation
------------
Install the package via the package control (CMS Made Simple) or clone the contents of the repo in your Sublime Text 2 package directory.

Usage
-----
+ **PHP Files:** Begin typing the name of the method you would like to use. The auto-completion menu will appear. Select the desired function from the list. Most all methods have placeholders. You can cycle through the placeholders using the tab key. A list of all the available CMSModule class methods can be viewed here:
http://apidoc.cmsmadesimple.org/CMS/CMSModule.html

+ **Smarty Files (*.tpl):** Type the full name of the snippet followed by the tab key.

Available Snippets
------------------
###PHP
+ **cms_db** - `$db = cmsms()->GetDb();`
+ **cms_dict** - `$dict = NewDataDictionary($db);`
+ **cms_loop**
```
while($results && $row = $results->FetchRow())
{
	$onerow = stdClass;
	$onerow->name = $row['name'];
	
	$entryarray[] = $onerow;
}
```
+ **cms_getmod** - `$mod = cms_utils::get_module('module_name');`
+ **get_tabopt** - `$taboptarray = array('mysql' => 'TYPE=MyISAM');`
+ **cms_createtab**
```
$sqlarray = $dict->CreateTableSQL(cms_db_prefix()."tablename", 
		$flds, $taboptarray);
$dict->ExecuteSQLArray($sqlarray);
```
+ **cms_getconfig** - `$config = cmsms()->GetConfig();`
+ **cms_getsmarty** - `$smarty = cms_utils::get_smarty();`
+ **cms_createtabindex**
```
$sqlarray = $dict->CreateIndexSQL(cms_db_prefix().'index_name',
				  cms_db_prefix().'table_name',
				  'column_name');
$dict->ExecuteSQLArray($sqlarray);
```
+ **cms_db_sql** - `$db->sql;`
+ **cms_db_error** - `$db->ErrorMsg();`
+ **cms_db_getone** - `$db->GetOne($query,array(value,value));`
+ **cms_db_execute** - `$db->Execute($query,array(value,value));`
+ **cms_db_fetchrow** - `$results->FetchRow();`

###Smarty
+ **smarty_form** 
```
{$startform}
<div class="pageoverflow">
	<p class="pagetext">{$prompt_name}</p>
	<p class="pageinput">{$input_name}</p>
</div>

<div class="pageoverflow">
	<p class="pagetext">&nbsp;</p>
	<p class="pageinput">{$submit} {$cancel} {$apply}</p>
</div>
{$endform}
```
+ **smarty_table**
```
<table cellspacing="0" class="pagetable">
	<thead>
		<tr>
			<th>Heading 1</th>
			<th>Heading 2</th>
			<th>Heading 3</th>
			<th>Heading 4</th>
			<th>Heading 5</th>
			<th class="pageicon">&nbsp;</th>
			<th class="pageicon">&nbsp;</th>
			<th class="pageicon">&nbsp;</th>
			<th class="pageicon">&nbsp;</th>
		</tr>
	</thead>
	<tbody>
		{$foreach from=$items key=key item=entry}
		{cycle values="row1,row2" assign='rowclass'}
		<tr class="{$rowclass}">
			<td>{$entry->one}</td>
			<td>{$entry->two}</td>
			<td>{$entry->three}</td>
			<td>{$entry->four}</td>
			<td>{$entry->five}</td>
			<td>{$entry->six}</td>
			<td>{$entry->seven}</td>
			<td>{$entry->eight}</td>
			<td>{$entry->nine}</td>
		</tr>
		{/foreach}
	</tbody>
</table>
```
+ **smarty_foreach**
```
{foreach from=$items key=key item=entry name=name}
	{$entry->item}
	
{/foreach}
```
Author
------
**Ben Bonora**
+ http://twitter.com/bbonora
+ http://github.com/bbonora
+ http://www.bennyvbonora.com

