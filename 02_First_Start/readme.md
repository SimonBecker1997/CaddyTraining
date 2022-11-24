# First Start of Caddy
## Before you start the lab
You've installed Caddy with apt or dnf. Therefor caddy is running as a service and must be stopped before running the next labs.
Do that by running:
```systemctl stop caddy```
## Start Caddy
```
caddy run
```
Nothing will happen now since we do not have any configuration. 
Then open a second command prompt and run the command
```
curl localhost:2019/config/
```
The response will look like this:
```
null
```
## Adding a first config
Create a file called `mysite.json`.  
Use the following command to do so: `touch mysite.json`.  
Open the file with an editor, for example nano: `nano mysite.json`.  
Enter the following code into the file:
```
{
	"apps": {
		"http": {
			"servers": {
				"example": {
					"listen": [":444"],
					"routes": [
						{
							"handle": [{
								"handler": "static_response",
								"body": "Hello, I am your first Website!"
							}]
						}
					]
				}
			}
		}
	}
}

```
Then, launch caddy by running: 
```
curl localhost:2019/load \
	-H "Content-Type: application/json" \
	-d @mysite.json
```
You can verify your config, by running `curl localhost:2019/config/`.  
By checking your Browser, you will still see a 404, not found, but in the command prompt you will get a response:
Run `curl localhost:444`.
The response will be:
```
Hello, I am your first Website!
```
