# Nginx L7 DDoS Protection!
Now easier then before, you will have to compile only Nginx, Rest of modules come pre-compiled.

- [x] Support Ubuntu 20.04.
- [x] Support Ubuntu 22.04.1

-- Security Dynamic Modules.
 - [x] ModSecurity Support.
 - [x] Naxsi Support.
 - [x] Lua Support.
 - [x] Cookie Based Challenge.
 - [x] [MOD LIST X Ubuntu 20.04](https://github.com/theraw/The-World-Is-Yours/tree/master/static/Focal/mod)
 - [x] [MOD LIST X Ubuntu 22.04](https://github.com/theraw/The-World-Is-Yours/tree/master/static/Jammy/mod)
 - [x] [Versions](https://github.com/theraw/The-World-Is-Yours/blob/master/version)
 
How do these 3 modules work together? L7 will block all or most of bots, ModSecurity and Naxsi take priority over cookie challenge!
So if its a offensive request that Modsecurity or Naxsi detect it as such then these 2 will deal with that request otherwise cookie challenge will appear.

## INSTALLATION

1. ```bash apt-get update; apt-get -y install build-essential libssl-dev curl nano wget zip unzip sudo git psmisc tar```

2. **`curl -s https://raw.githubusercontent.com/theraw/The-World-Is-Yours/master/install > install; bash install`**


## Basic info.

```
=> Nginx Folder     = /nginx/
=> --conf-path      = /nginx/nginx.conf
=> --pid-path       = /var/run/nginx.pid 
=> --user           = nginx 
=> --group          = nginx
=> --sbin-path      = /usr/sbin/nginx
=> --error-log-path = /var/log/nginx/error.log

LUA RESTY CORE SCRIPTS = /usr/twiylua/

// YOUR NGINX IS LOCATED AT /nginx NOT /etc/nginx
```


## KEEP IN MIND!
1. You're trading perfomance for security.
2. If your server provider does not have anti-ddos your IPTABLES will fail to keep the bans, and your server may be offline in cases of big attacks.
3. This is not a script that with one command your ddos problem is fixed, there's no such thing for L7 attacks as they change and new methods come out very often and no one has any ideas where your server is lacking security so this script is a basic thing more advanced protection require knowledge, monitoring logs, and applying filters in order to automatically ban attackers, this project is suggested to run with fail2ban + iptables.

