---
layout:     post
title:      Install php composer on mac
subtitle:   
date:       2020-02-24
author:     CodingDonkey
header-img: 
catalog: true
tags:
    - PHP
---


Composer is a cross-platform dependency manager for PHP libraries.

In this guide, i'm installing Composer on a machine running Mac OSX with MAMP.

1. Open a terminal and navigate to your user directory, ie cd /User/<USER_NAME>/
2. Run this command shown below to download Composer. This will create a Phar (PHP Archive) file called composer.phar:

  `curl -sS https://getcomposer.org/installer | php`

3. Now we move composer.phar file to a directory

	`sudo mv composer.phar /usr/local/bin/`

4. We want to run Composer with having to be root al the time, so we need to change the permissions:

	`sudo chmod 755 /usr/local/bin/composer.phar`
 

5. Next, we need to let Bash know where to execute Composer: 
	` nano ~/.bash_profile`

6. Add this line below to bash_profile and save
 

	` alias composer="php /usr/local/bin/composer.phar"`

7. and then run this command:
 

	`source ~/.bash_profile`
 

8. Finally, run: 
	`composer --version`
If all goes well and it is working, you'll see this screen:
	` Composer installed`
