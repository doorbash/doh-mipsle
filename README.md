## Build
```
GOOS=linux GOARCH=mipsle GOMIPS=softfloat go build -trimpath -ldflags="-s -w" -o doh-mipsle
```

## Usage
```
./doh-mipsle [OPTIONS]
```

**Options:**
```
  -debug
        print debug logs
  -dns string
        Custom DNS. Example: 8.8.8.8:53
  -dohserver string
        DNS Over HTTPS server address (default "https://mozilla.cloudflare-dns.com/dns-query")
  -host string
        interface to listen on (default "localhost")
  -port int
        dns port to listen on (default 5353)
```

## Example
```
./doh-mipsle
./doh-mipsle --host=127.0.0.1 --port=5353
./doh-mipsle --host=127.0.0.1 --port=5353 --dns=8.8.8.8:53
```