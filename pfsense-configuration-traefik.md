# Adding PFsense to traefik

### Make sure you have your PFsense FQDN added to your local DNS resolver/forwarder.

1. Add your pfsense IP/HOSTNAME to your .env file and uncomment the line

![image](https://user-images.githubusercontent.com/1687761/180992872-63bf1ac2-d414-4384-bd69-94b8b81e0b5f.png)

2. Enable the external service using :
 
```
make enable-external pfsense
```


## Avoiding DNS Rebind errors for PFsense when used with traefik

#### Add your FQDN to your PFsense as a hostname 

1. Go to System and then General Setup

![image](https://user-images.githubusercontent.com/1687761/180988066-667a2e76-eb22-40f0-9f5e-1e7600b1b8ae.png)

#### (Optional) Adding alternate hostnames for PFsense

1. Go to System and then Advanced and then Admin Access 

![image](https://user-images.githubusercontent.com/1687761/180989245-fa7c8c98-51b3-44fb-804d-8c7290dcf94f.png)

2. Find alternate hostnames

![image](https://user-images.githubusercontent.com/1687761/180988304-be7d269f-0c07-4c6e-8006-2cbe5be515de.png)

## (Optional) Change the port of the PFsense webConfigurator

1. Go to the same page as described in the optional setup above and find TCP port

![image](https://user-images.githubusercontent.com/1687761/180989672-fe6ecae1-d6ec-499e-934f-fface247647d.png)

2. Add your port to your .env file 

![image](https://user-images.githubusercontent.com/1687761/180990245-e38f7f6f-3651-44b3-aa60-5007639b51dd.png)

3. Run Make to refresh traefik
4. Done
