# cors-anywhere

See upstream for more documentation.

### Setup

`npm install`
`npm start`

### Nginx Configuration

```nginx
location /corsproxy/ {
      if ($request_uri ~ ^/corsproxy/(.*) ) {
          set $cors_request_uri $1;
      }

      proxy_pass http://127.0.0.1:1234/$cors_request_uri;
      proxy_buffering off;
}
```

### Usage

1) https://example.com/corsproxy/https://cdn.discordapp.com/attachments/746507379310461010/1078547095469953084/1677213954391441.png

2) https://example.com/corsproxy/www.google.com
