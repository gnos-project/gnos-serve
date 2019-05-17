# GNOS Serve

Quickly serve current directory to LAN or Internet

- HTTP/HTTPS + FTP (read-only + write) protocols support
- HTTP/HTTPS reverse tunneling ([serveo](https://serveo.net) + [ngrok](https://ngrok.com))
- Authenticated + Anonymous support
- Network interface + TCP port binding

## Usage

```
Usage: srv [options] [ PORT | --ngrok | --serveo [NAME] ]

               PORT    Listening tcp, default: $port
  -b, --bind   BIND    Listening ip, default: $bind
  -u, --user   USER    Authentication username
  -p, --pass   PASS    Authentication password
  -f, --ftp            Use FTP protocol, read-only
  -F, --ftpw           Use FTP protocol with WRITE perms
  -S, --http           Use HTTP protocol instead of HTTPS
  -N, --ngrok          Use https://ngrok.com reverse-tunneling
  -n, --serveo [NAME]  Use https://serveo.net reverse-tunneling
```

## Install

Just copy somewhere in your `$PATH`.

### Dependencies

- python
- sauth: `sudo pip install sauth`
- pyftpdlib: `sudo pip install pyftpdlib`
- ngrok: <https://ngrok.com/download>
- serveo: `sudo pip install autossh`, OPTIONAL degrades to ssh
