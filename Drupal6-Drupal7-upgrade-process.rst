
Document Information
====================

Name of the Document: Drupal 6 to Drupal 7 upgradation process

Date: 7/04/2015

Author: Priyanka Bhagwat and Prashant Sinalakar

----------------------------------------------------------------------------------------------------------------------------
**Process to upgrade from drupal 6 to drupal 7**
-----------------------------
**step 1:**

**take a backup of your drupal site and database**
-----------------------------
**step 2:**


**Login as superuser/first user and disable all custom modules and
custom theme of drupal 6 site.**
-----------------------------
**step 3:**

	1) **Install drush into your system**

	sudo apt-get install drush

	2) **Download latest version of drupal**

	drush dl drupal-7

	3) **Connect your existing drupal 6 database with new drupal 7** (make
	       changes in setting.php of drupal 7 to connect with old database)

	4) **Go to project directory then run**

	drush updb

	5) **Login in to drupal 7 as first user**

	6) **move all old site data to new drupal 7 expect theme**

	7) **remove modulename\_bck modules**

	8) **update all modules using**

	drush dl -y acl references author\_pane ckeditor votingapi views ctools
	references xmlsitemap webform advanced\_forum captcha cck ckeditor
	comment\_notify email\_verify extlink feedback fivestar formblock
	google\_analytics jquery\_ui jquery\_update link linkchecker masquerade
	mimemail nice\_menus notify recaptcha spambot views

	drush dl -y views date easy\_social captcha cck email\_verify sharethis
	socila\_share wysiwyg google\_analytics jquery\_ui link masquerade
	recaptcha

	9) enable all necessary modules

	drush en module\_name

	drush updb

	if any error in webform take out webform form modules then,

	**drush updb**

	**drush command to update all modules without updating the core.**

	drush upc --no-core

-----------------------------
**step 4:**

	1) drush dl drupal-7

	2) make settings.php

	3) connect with old db

	then, go to project dir run

	4) # references, link

	5) drush updb
-----------------------------

**step 5:**

	1) login to first user

	2) mv all old sites data to new d7 except theme

	3) remove modulename\_bck modules

	them update all modules using

	drush dl -y acl references author\_pane ckeditor votingapi views ctools
	references xmlsitemap webform advanced\_forum captcha cck ckeditor
	comment\_notify email\_verify extlink feedback fivestar formblock
	google\_analytics jquery\_ui jquery\_update link linkchecker masquerade
	mimemail nice\_menus notify recaptcha spambot views

	## acl references views ctools references webform cck link views

	4) enable all necessary moduls

	5) drush updb

	if any error in webform take out webform form modules then,

	drush updb

	node\_access => references

-----------------------------
**step 6:**
	Only for SCILAB Website
	Scilink Query

	content type => Documentation Page

	select \* from content\_field\_link where nid in (SELECT nid FROM
	\`content\_type\_link\` where \`field\_parent\_page\_nid\`=118)
-----------------------------
**Important**

	1) **changed query structure..**

	2) **theme\_table must be replaced to ‘theme(“”, “”, array =()) **
-----------------------------
***Error and solution :***

	**If you get error like following: **

	**“Undefined index: distribution\_name in
	drupal\_install\_profile\_distribution\_name() (line 207 of
	/var/www/html/drupal-7.37/includes/install.inc “**

	**Then run following query in database**

	`***UPDATE*** <http://dev.mysql.com/doc/refman/5.5/en/update.html>`__
	`***system*** <http://localhost/adminer/adminer.php?username=root&db=anuduino_os_hardware_in&table=system>`__
	**`*SET* <http://dev.mysql.com/doc/refman/5.5/en/string-type-overview.html>`__
	status=1 WHERE name='standard';**

	**This will resolve profile error**

	**While going for changing query of theme**

	theme('table', array('header' => $pending\_header, 'rows' =>
	$pending\_rows ));

	solve error of mail sending: email.inc change following line

	change

	**$language-language** replace with **array('language' =>
	$language->language)**

	**$message['body'] = t('…...’);** replace with **$message['body'] =
	array('body' => t('…….));**

	**Error:** *Notice*: Undefined index: distribution\_name in
	*drupal\_install\_profile\_distribution\_name()* (line *207* of
	*/var/www/html/cfd\_fossee\_in\_7/includes/install.inc*).

	FIX this:

	UPDATE \`drupal\`.\`system\` SET \`status\` = '1' WHERE
	\`system\`.\`filename\` = 'profiles/standard/standard.profile';
