Slide: [[AWS Certified Solutions Architect Slides v40.pdf#page=148|AWS Certified Solutions Architect Slides v40, page 148]]

SSL/TLS basics:
- Used to encrypt in-fight traffic (https means connection is encrypted using ssl/tls)
- SSL: Secure Socket Layer (older)
- TLS: Transport Layer Security (newer)
- SSL certs can be expired and need renewal


The LB can do **SSL termination**: meaning the connection from client -> LB is encrypted (https), but behind the LB, services can connect using http.

LB SSL cert:
- Use  SSL/TLS server certificate (X.509)
- Clients can use SNI (Server Name Indication) [[AWS Certified Solutions Architect Slides v40.pdf#page=150&selection=8,0,12,28|AWS Certified Solutions Architect Slides v40, page 150]] to indicate the target server

SNI: is basically a way to incorporate the domain of the target server into the handshake. When client connect to LB, LB looks at the cert then forward the traffic to the target.

Multiple listener and SSL/TLS cert support: [[AWS Certified Solutions Architect Slides v40.pdf#page=150|AWS Certified Solutions Architect Slides v40, page 150]]