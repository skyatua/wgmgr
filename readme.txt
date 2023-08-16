
## Wireguard VPN manager

### Install

```
git clone https://github.com/skyatua/wgmgr.git
```
### Create settings file

```
cd wgmgr
cat << EOF > vars
IF="<if name>"
IP4="ip4/cidr"
IP6="ip6/cidr"
MTU="1420"
SAVECONFIG="true"
LISTENPORT="51820"
SERVER_IP="public ip"
DNS="dns, dns, ..."
PEER_ALLOWEDIPs="ip/cidr, ip/cidr, ..."
PEER_PERSISTENTKEEPALIVE="25"
EOF
```

### Create server configuration

```
wgmanager --server
```

### Add Peer configuration
```
wgmanager --peer "test" --ip "ip/cidr"
```

