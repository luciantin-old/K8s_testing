# Ingress
- External Service vs Ingress ?

- Ingresses operate at layer 7 (application layer), it can also provide features like cookie-based session, which is not possible via services.

- Ingress gives you one entry point into the cluster but allows you to access multiple services that are exposed in the ingress definition
  whereas if you have to expose multiple services without using an ingress you'll have to manage/remember all of their externalIPs individually.
  
- An ingress controller also extends L4/L7 capabilities on top of your service for things like TLS, while/blacklisting IPs, etc

- ingress redirects requestes to internal services without exposing ports and ip addresses