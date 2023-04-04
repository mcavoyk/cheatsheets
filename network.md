# Network

### UDP Server

```bash
socat - udp4-listen:5000,reuseaddr,fork
```

### UDP Client

```bash
echo "hello" | socat -t 1 - udp4-sendto:127.0.0.1:5000
```

### Monitor Network Interface

```bash
tcpdump -i {{lo}}
```


### Monitor Network Interface and Port

```bash
tcpdump -i {{lo}} port 5000
```
