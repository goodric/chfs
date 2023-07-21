# Cute File Explorer （chfs）共享文件系统存在跨站脚本攻击漏洞

## Description:
Cute Http File Server (chfs) is a free, HTTP protocol file sharing server that can be accessed quickly using a browser.
Due to incorrect configuration, the hacker logs in to the chfs background using the default password and fails to verify the user input in the file search box. As a result, malicious data can be constructed to cause cross-site scripting attacks.

## chfs website:
http://iscute.cn/chfs
Latest version 2.0

## using：
Login interface

The weak password is used to successfully log in to the file sharing system

Try to construct a cross-site scripting attack statement in the file search box

Successful popup
