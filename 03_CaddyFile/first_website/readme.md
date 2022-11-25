# Serving your first website with Caddy
Prerequisites: This lab just works with a VM and a domain attached to it.
## Lab 1: Serve a simple index.html file
1. Copy the content of the Caddyfile into your freshly created Caddyfile. Change the Domain in the caddyfile to your domain
2. Create the corresponding folder in /var/www by executing the following command:
```
mkdir /var/www/mywebsite
```
3. Create an index.html in the created folder by running `touch /var/www/mywebsite/index.html`
4. Use any editor, for example nano to edit the file content. Add any content you like
5. Start Caddy with the command `caddy run`
## Lab 2: Serve a sample website
1. after running your index html, stop caddy by hitting `ctrl + c` on your keyboard
2. Clone the github repository and copy the demo folder to your `/var/www/mywebsite` directory
3. Run caddy again with the command `caddy run`
