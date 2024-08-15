LAMPX = Linux Apache MySQL PHP XDebug

Install
[[Apache2]{.underline}](https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-20-04)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>sudo apt update<br />
sudo apt install apache2<br />
sudo ufw app list<br />
sudo ufw allow 'Apache Full'<br />
sudo systemctl restart apache2<br />
sudo systemctl status apache2</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

SSL On Localhost Can be Installed By Following this
[[Article]{.underline}](https://www.arubacloud.com/tutorial/how-to-enable-https-protocol-with-apache-2-on-ubuntu-20-04.aspx).

Install
[[Nginx]{.underline}](https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-20-04)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>sudo apt update<br />
sudo apt install nginx</p>
<p>sudo ufw allow 'Nginx Full'</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Install
[[MySQL]{.underline}](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>sudo apt update<br />
sudo apt install mysql-server<br />
sudo systemctl start mysql.service<br />
sudo mysql<br />
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY
'&lt;enter-custom-password&gt;';</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Install
[[PHP]{.underline}](https://www.digitalocean.com/community/tutorials/how-to-install-php-7-4-and-set-up-a-local-development-environment-on-ubuntu-20-04)

First of all, on fresh Ubuntu you don\'t directly install php, it's
required to add an ondrej php repository in order to work with multiple
php versions.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>sudo apt-get update<br />
sudo apt -y install software-properties-common<br />
sudo add-apt-repository ppa:ondrej/php<br />
sudo apt-get update</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>getphp(){<br />
echo "Enter PHP Version like: 7.0 , 7.1 , 7.2 , 7.3, 7.4, 8.0, 8.1
etc!";<br />
read phpVersion<br />
sudo apt update<br />
sudo apt install php$phpVersion libapache2-mod-php$phpVersion
php$phpVersion-mysql php$phpVersion-fpm php$phpVersion-mbstring
php$phpVersion-bcmath php$phpVersion-intl php$phpVersion-soap \<br />
php$phpVersion-zip php$phpVersion-gd php$phpVersion-json
php$phpVersion-curl php$phpVersion-cli php$phpVersion-xml
php$phpVersion-xmlrpc php$phpVersion-gmp \<br />
php$phpVersion-common<br />
sudo phpenmod mbstring<br />
sudo phpenmod pdo_mysql<br />
sudo a2enmod proxy_fcgi setenvif<br />
sudo a2enconf php$phpVersion-fpm<br />
sudo a2enmod rewrite<br />
sudo systemctl restart apache2<br />
}</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Paste above snippet on the terminal & fire the command "getphp".

Note : It may conflict with php8.1 or higher versions so you can remove
the buggy extension from above function and try again.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>enablephp(){<br />
echo "Enter PHP Version like: 7.0 , 7.1 , 7.2 , 7.3, 7.4, 8.0, 8.1
etc!";<br />
read phpVersion<br />
a2dismod php*.*<br />
a2enmod php$phpVersion<br />
systemctl restart apache2<br />
}<br />
<br />
alias setphp="sudo update-alternatives --config php;sudo
update-alternatives --config phar;update-alternatives --config
phar.phar;a2dismod php*.*;systemctl restart apache2;enablephp"</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

To set default php version for using over the terminal and on browser
localhost's info.php file, paste above snippet code over the terminal
and fire the command "setphp".

Install **Xdebug**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>getxdebug(){<br />
echo "Enter PHP Version like: 7.0 , 7.1 , 7.2 , 7.3, 7.4, 8.0, 8.1
etc!";<br />
read phpVersion<br />
sudo apt update<br />
sudo apt install php$phpVersion-xdebug<br />
echo -e "zend_extension =
xdebug.so\nxdebug.mode=develop,debug\nxdebug.start_with_request=yes\nxdebug.client_port=9003"
&gt; /etc/php/$phpVersion/mods-available/xdebug.ini<br />
sudo systemctl restart apache2<br />
}</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Paste above code snippet over the terminal and fire command "getxdebug".
Please put the required php version value.

Install [[Chrome
Extension]{.underline}](https://chrome.google.com/webstore/detail/xdebug-helper/eadndfjplgieldjbigjakmdgkmoaaaoc)
For Xdebug.

Install [[VS Code
Extension]{.underline}](https://marketplace.visualstudio.com/items?itemName=xdebug.php-debug)
For Xdebug.

Install
[[Composer]{.underline}](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-composer-on-ubuntu-20-04#step-2-downloading-and-installing-composer)

Install
[[ElasticSearch]{.underline}](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-elasticsearch-on-ubuntu-20-04)

Install
[[NodeJs]{.underline}](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04)
