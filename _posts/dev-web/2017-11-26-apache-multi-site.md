---
layout: post
title:  "Configuration multi-sites via apache"
date:   2017-11-26 23:00 +0200
category: dev-web
---

- [Configure the domain name](#configure-the-domain-name)
- [Configure Apache](#configure-apache)
- [Enable site](#enable-site)

# Configure the domain name
[Go to Manage Freenom DNS](https://www.my.freenom.com)

![freenom](/image/freenom.png)

Replace jeanneret.tk with the domain name.

# Configure Apache
Copy the jeanneret.tk.conf to domainname.tk.conf
Then change the ServerName, ServerAlias and DocumentRoot

```bash
<VirtualHost *:80>
	ServerAdmin admin@ServerName.tk
	ServerName domainname.tk
	ServerAlias www.domainname.tk
	DocumentRoot /var/www/domainname.tk
	ErrorLog ${APACHE_LOG_DIR}/error.log
	CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

# Enable site
Then we have to enable the site with :
```bash
sudo a2ensite domainname.tk.conf
sudo service apache2 restart
```

DNS change can take up to 24 hours.