# How to add a new service to authentik via docker lables and traefik middlewares

1. First you need to add the label to the application in question

```
- traefik.http.routers.whoami.middlewares=authentik@docker
```

2. Once you have added the label, you need to add the application to authentik. To do this you need to go to the admin interface of Authentik

![image](https://user-images.githubusercontent.com/1687761/181040353-788011f4-410c-4cd7-a01d-48bb2d66e5b4.png)


![authentik application ](https://user-images.githubusercontent.com/1687761/181040166-e52bbb77-4805-4935-a201-11d3c45056e7.png)

3. Then you need to create a provider 

![image](https://user-images.githubusercontent.com/1687761/181042386-2de6363d-30ac-4ccf-8b0d-484dcada02d7.png)

4. After you have created a provider and a application, then you will have to add the provider to the outpost


![authentik outpost config ](https://user-images.githubusercontent.com/1687761/181042682-40e299af-8d78-4077-bf4f-c773a4df79b5.png)

5. Make sure it is selected in gray

6. Try to log in

7. Done
