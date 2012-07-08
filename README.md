# locknet

locknet is a simple firewall/proxy script you can use to tunnel all your network
traffic through a single SSH connection. When you run it, it tells iptables to
block all network traffic except to the IP/port of your proxy host, opens an SSH
connection to that host with `DynamicForward 1080` (and my own `LocalForward`s,
which you probably want to change), and changes GNOME's proxy settings to use
it. When you kill locknet, the connection dies and it restores your old network
settings.
