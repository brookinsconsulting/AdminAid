AdminAid Usage
=============

o What is AdminAid

AdminAid started as a simple module to be able to switch users
easily while debugging. After that I decided to extend it a little,
and make a proper extension out of it. Today you can also view 
detailed content object data, and a list of all objects based on
a class. Latest addition is a class translation tool.
More functionality may come in the future.

I do not recommend using this extension on live servers for more
than a limited timespan. It does represent a potential security
risk, even though in theory it should be secure. You are hereby warned.


o Using the AdminAid extension

The following functions are available:

* User switching: Switch user from administrator to any other in
the system, without a password.

In admin interface you can click on a users icon to get the 
drop down menu, and select the Switch User command.

You can also write the url directly, either in admin or frontend:
http://<site>/aid/user_switch/<user_id>

There are a built in security check, the user who need access to this 
function must be specified by user id in the ini file:
extension/admin_aid/settings/aid.ini.append.php

* Object view: Get an overview of the data in any object, with more
information from the database.

In admin interface you can click on an objects icon to get the 
drop down menu, and select the View Object Details command.

You can also write the url directly, either in admin or frontend:
http://<site>/aid/object_view/<object_id>

The information shown will contain object remote id, published/modified
dates, list of nodes and their remote id's, a version list, and a 
more detailed list of all attributes of the object. The attributes
names also contain a tooltip with id's.

* Object list: List all objects of one class

In admin interface you can go to the class view page, there will be
a link on the Object count. Click on this link to see a list of all
objects based on this class.

You can also write the url directly, either in admin or frontend:
http://<site>/aid/object_list/<class_id>

* Translate class: Translate a class on all languages in the same page.

At the class view page there is a button "Translate on all languages"
under the attribute list frame. Clicking this you come to a page that
lets you edit translations for all languages of the class at the same
time.

You can also add any new languages that your database support to the
class, by checking the appropriate checkboxes in the bottom of the page,
and clicking "Add language".

In addition you can copy translations from an attribute in a different
class. This is practical for general attributes like "Name" or 
"Description". You do this by clicking the "Copy translations from other
attribute" button. Then you select the attribute you wish to copy from.
AdminAid will pr.default "guess" which attribute you want, by selecting
one that have the same identifier. After selecting the attribute, you
are required to click the "Apply" button to store the copied translation.

Note that when editing translations, the class is not set in edit mode.
This means that another person can edit the class at the same time that
you do translations on it, which might create a conflict. Also, every
time you press the "Ok" or "Apply" buttons, the new translations are
immediately published and available to the system.

