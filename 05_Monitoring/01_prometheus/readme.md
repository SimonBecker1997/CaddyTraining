# Prometheus Monitoring
Caddy supports exposing metrics in a prometheus endpoint.
This endpoint will be awailable on `localhost:2019/metrics`

## Lab
Use the existing Caddyfile of this folder or create a new one with the following content
```
{
    servers {
        metrics
    }
}

training-it-consulting-becker.de {
        respond "Hello, I am a website"
}

```

Start caddy with `caddy run`

Open a second command prompt and run `curl localhost:2019/metrics`
