# The Cute File Explorer (chfs) shared file system has a reflection cross-site scripting vulnerability

## Description:
Cute Http File Server (chfs) is a free, HTTP protocol file sharing server that can be accessed quickly using a browser.
Due to incorrect configuration, the hacker logs in to the chfs background using the default password and fails to verify the user input in the file search box. As a result, malicious data can be constructed to cause cross-site scripting attacks.

## chfs website:
http://iscute.cn/chfs
Latest version 2.0

## using：
example url：
http://47.104.157.204:10000/
Due to incorrect configuration, anonymous users can directly access the main interface of the file sharing system without logging in, that is, they have any file reading permission of the file sharing service
![Image](https://github.com/goodric/chfs/assets/76898521/f6ef5da4-df3e-4cdd-93fe-716a72a90813)

Observe the effect of the search file box.
![Image](https://github.com/goodric/chfs/assets/76898521/cfcd0dd3-e014-44cf-b069-bdf3e7f487f1)


Try to construct a cross-site scripting attack statement in the file search box
Successful popup
![Image](https://github.com/goodric/chfs/assets/76898521/f5666174-1194-4081-84b5-8a3d7075bc64)

## Fix:
Strict verification of user input
