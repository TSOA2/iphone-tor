# Setting up TOR on your iPhone

Recently I've become intrigued by the TOR browser, and I got sidetracked trying to use my iPhone with it. Not all the stuff I put in this README will be accurate or the "best practice", so beware. I made this for myself in the future, but if you need it, you can try as well.

## Setting up the `tor` socks5 proxy

 - `sudo apt install tor`
 - `tor` (no options)

## Setting up the `htps` http proxy

Due to iPhone not being able to use `socks` proxies, you have to use an HTTP proxy. Luckily, after a quick Google search, I found [http-proxy-to-socks](https://github.com/oyyd/http-proxy-to-socks), which is a tool to "convert SOCKS proxy into http proxy".

 - `sudo npm install -g http-proxy-to-socks`
 - `htps -s 127.0.0.1:9050 -l [your-ip-address] -p 8080`

Obviously replace [your-ip-address] with your actual IP address.

## Using it on your iPhone

 - Go to Settings -> Wi-Fi -> [your-wifi]
 - Scroll to the bottom
 - Where it says "Configure Proxy" under "HTTP Proxy", tap it and go to Manual.
 - Enter your IP address into the "Server" field, and in the "Port" field, enter "8080".

## Done!

You probably shouldn't do this. :)
