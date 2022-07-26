# How to add a new service to authelia via docker lables and traefik middlewares

0. Remember to generate a new password for your authelia user in the users_database.yml / Reset it and set a new one

1. First you need to add the label to the application in question

```
# Remember to change the service name here (whoami for your service)

- traefik.http.routers.whoami.middlewares=authelia@docker
```

2. Once you have added the label, you need to add the application to authelia. 

3. Open the configuration.yml in the authelia etc folder

4. Find access_control
5. Add your service 

```
    - domain: whoami.yourhostname.tld
      policy: one_factor

```

6. Run make

```
make
```
