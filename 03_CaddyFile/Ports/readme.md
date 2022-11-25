# Serving multiple websites via ports
## Lab
1. Create a Caddyfile and copy the following content into it:
```
localhost:9999 {
  root * /var/www/site1
  file_server

localhost:9998 {
  root * /var/www/site2
  file_server
}
```
2. Create the directorys at `/var/www/`:
```
mkdir -p /var/www/site1 && mkdir -p /var/www/site2
```
3. Create the index.html files: 
```
touch /var/www/site1/index.html && touch /var/www/site2/index.html
```
4. Fill the html files with any content you like
5. Start Caddy by running `caddy run`
