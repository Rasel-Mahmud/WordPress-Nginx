#  WordPress on Ubuntu 20.04 with Nginx | PHP (7.4) | Let’s Encrypt

Credit
1. https://websiteforstudents.com/how-to-install-wordpress-on-ubuntu-20-04-18-04-with-nginx-and-lets-encrypt/
2. https://gist.github.com/amanjuman/21a439d4dfad68dbad9245ff1a18bf1e

See the `wordpress.txt` file for details

Here is the solution for login mysql in 3rd party client
https://askubuntu.com/questions/1029177/error-1698-28000-access-denied-for-user-rootlocalhost-at-ubuntu-18-04

MySQL or Maria DB Command:
https://www.cyberciti.biz/faq/how-to-show-list-users-in-a-mysql-mariadb-database/

Import and Export DB link:
https://www.digitalocean.com/community/tutorials/how-to-backup-mysql-databases-on-an-ubuntu-vps

Change table with new URL:

`UPDATE wp_options SET option_value = replace(option_value, 'oldlink.com', 'newlink.com') WHERE option_name = 'home' OR option_name = 'siteurl';
UPDATE wp_posts SET guid = replace(guid, 'oldlink.com','newlink.com');
UPDATE wp_posts SET post_content = replace(post_content, 'oldlink.com', 'newlink.com');
UPDATE wp_postmeta SET meta_value = replace(meta_value,'oldlink.com','newlink.com');
UPDATE wp_options SET option_value = replace(option_value, 'oldlink.com', 'newlink.com') WHERE option_name = 'home' OR option_name = 'siteurl';
UPDATE wp_posts SET guid = replace(guid, 'oldlink.com','newlink.com');
UPDATE wp_posts SET post_content = replace(post_content, 'oldlink.com', 'newlink.com');
UPDATE wp_postmeta SET meta_value = replace(meta_value,'oldlink.com','newlink.com');`

Link: https://codepen.io/EightArmsHQ/full/nzEjI

WordPress Admin MD5 Pass Genarator: https://www.useotools.com/wordpress-password-hash-generator/
