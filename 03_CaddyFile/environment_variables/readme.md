# Environment Variables
Run in your command Prompt: 
```
export SITE_URL=your-website.com
```
Replace your-website.com with your real adress

Create a Caddyfile with the following content:
```
4{SITE_URL} {
        respond "Hello, I am Website with environment variable"
}
```
