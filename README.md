# LAMP Stack Setup on macOS (iMac 2021)

## System Information
- Device: iMac 2021
- OS: macOS
- Package Manager: Homebrew

---

## 1. Homebrew Installation

To verify Homebrew installation:

```bash
brew --version
```

---

## 2. MySQL Installation

Install MySQL using Homebrew:

```bash
brew install mysql
```

Start MySQL service:

```bash
brew services start mysql
```

Verify MySQL version:

```bash
mysql --version
```

Check running services:

```bash
brew services list
```

---

## 3. Apache (Pre-Installed on macOS)

Apache is pre-installed by default on macOS.

Check Apache version:

```bash
httpd -v
```

Example output:

```
Server version: Apache/2.4.62 (Unix)
```

Start Apache:

```bash
sudo apachectl start
```

Verify Apache is running:

```bash
ps aux | grep httpd
```

Test in browser:

```
http://localhost
```

Terminal verification:

```bash
curl http://localhost
```

Expected output:

```html
<html><body><h1>It works!</h1></body></html>
```

---

## 4. PHP Installation

Install PHP using Homebrew:

```bash
brew install php
```

Verify PHP version:

```bash
php -v
```

Create a PHP test file:

```bash
sudo nano /Library/WebServer/Documents/info.php
```

Add the following:

```php
<?php
phpinfo();
?>
```

Save and exit.

Restart Apache:

```bash
sudo apachectl restart
```

Verify file exists:

```bash
ls -l /Library/WebServer/Documents/
```

Test PHP in browser:

```
http://localhost/info.php
```

---

## Conclusion

The LAMP stack (Apache, MySQL, PHP) was successfully installed and tested on macOS using Homebrew. Apache was verified using localhost, MySQL was confirmed running via Homebrew services, and PHP was tested using a phpinfo() file
