# The Cute File Explorer (chfs) shared file system has a reflection cross-site scripting vulnerability

## Description:
Cute Http File Server (chfs) is a free, HTTP protocol file sharing server that can be accessed quickly using a browser.
Due to incorrect configuration, the hacker logs in to the chfs background using the default password and fails to verify the user input in the file search box. As a result, malicious data can be constructed to cause cross-site scripting attacks.

## chfs website:
http://iscute.cn/chfs
Latest version 2.0

## using：
example url
http://47.104.157.204:10000/
-
Due to incorrect configuration, anonymous users can directly access the main interface of the file sharing system without logging in, that is, they have any file reading permission of the file sharing service

Observe the effect of the search file box.


Try to construct a cross-site scripting attack statement in the file search box
Successful popup

## Fix:
Strict verification of user input
