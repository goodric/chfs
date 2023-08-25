# The Cute File Explorer (chfs) shared file system has storage cross-site scripting vulnerabilities

## Description:
Cute Http File Server (chfs) is a free, HTTP protocol file sharing server that can be accessed quickly using a browser.
Because the content of the file is not limited enough, malicious data can be written into the file and accessed, resulting in cross-site scripting attacks.

## chfs website:
http://iscute.cn/chfs
Latest version 2.0

## using：
Due to configuration errors, anonymous users can directly access the main interface of the file sharing system without logging in, and have the permission to change any file of the file sharing service

Create a file that constructs malicious data in its contents

When you access the file page, the pop-up window of the cross-site scripting attack succeeds
/chfs/shared/2.php

## Fix:
Strict verification of user input
