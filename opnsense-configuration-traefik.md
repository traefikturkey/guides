# Adding Opnsense to traefik

### Make sure you have your OPNsense FQDN added to your local DNS resolver/forwarder.

1. Add your OPNsense IP/HOSTNAME to your .env file and uncomment the line

![image](https://user-images.githubusercontent.com/1687761/180999308-3a11a27d-97af-43c0-bedc-85a2f7cc6869.png)

2. Enable the external service using :
 
```
make enable-external opnsense
```


## Avoiding DNS Rebind errors for OPNsense when used with traefik

#### Add your FQDN to your OPNsense as a hostname 

1. Go to System and then Settings and then General

![image](https://user-images.githubusercontent.com/1687761/180999402-f7b65246-4e95-4e86-ab4c-de654ca0feff.png)

#### (Optional) Adding alternate hostnames for OPNsense
1. Go to System and then Settings and then Administration 

2. Find alternate hostnames

![image](https://user-images.githubusercontent.com/1687761/180999745-15979903-ae56-4f27-99f9-30236b4982c0.png)

## (Optional) Change the port of the OPNsense webConfigurator

1. Go to the same page as described in the optional setup above and find TCP port

![image](https://user-images.githubusercontent.com/1687761/181000196-1f7cc7ba-3b5b-491a-ab69-0e0597a233bc.png)


2. Add your port to your .env file 

![image](https://user-images.githubusercontent.com/1687761/181000255-61e2658b-bf82-45f2-92ad-393e5e69cd8c.png)


3. Run Make to refresh traefik
4. Done
