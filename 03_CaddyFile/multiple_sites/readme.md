# Run multiple Websites with subdomains with Caddy
Hint: This lab works just on a cloud VM with a domain attached to it. You cannot run it on localhost! 

## Run the lab
1. Copy the Caddyfile from this folder into your machine, or simply clone the repository.
2. Create Domain entries for the subdomains in your cloud providers WEB UI. (See in video on how to do that)
3. Adjust in the caddyfile the Domain Names to your Domain
4. Create 2 folders:
```
mkdir /var/www/website1 && mkdir /var/www/website2
```
5. Create 2 Index HTML files inside there:
```
touch /var/www/website1/index.html && /var/www/website2/index.html
```
6. Create some Content for both HTML files. It is up to you what to enter there :)
