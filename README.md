# go-font
This repository contains the Go font adapted for the web.

## Crostini Terminal
This is a short explanation on how to display the font in ChromeOS terminal:

We cannot add a new font to ChromeOS, but Secure Shell can be customized using CSS.
Since I want to display the font offline, it will be stored inside Crostini,
served with an HTTP server, and loaded with CSS into Secure Shell.

1. install a web server of your choice
2. clone this repo in your public folder
3. ensure that the file from the repo are served with CORS
    - for Caddy add `header /go-font/ Access-Control-Allow-Origin *`
4. hit `ctrl+shift+p` and set the police to `Go Mono`
5. add an `user-css` as `http://penguin.linux.test:3000/go-font/Go%20Mono.css`
