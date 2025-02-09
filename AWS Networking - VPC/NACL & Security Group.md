
![[nacl-vs-security-group.png]]

**Ephemeral Ports**
Client connects to **defined ports** and expect response to an **ephemeral port**, which typically opens for the duration of the request.
- IANA & MS Windows 10: 49152 -> 64435
- Many linux kernels: 32768 -> 60099

Example
![[ephemeral-ports-example.png]]

which is why when config NACL, we need to open for traffic from 1024 -> 65535