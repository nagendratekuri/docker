# Example - Host a simple HTML file using nginx image

```sh
docker run --name example -p 80:80 -v /home/ec2-user/html/:/usr/share/nginx/html:ro -d nginx
```

### Parameters
```sh
--name my-nginx-c1 : Assign a name to the container
--detach : Run container in background and print container ID
-v /home/vivek/html/:/usr/share/nginx/html:ro : Bind mount a volume
-p 80:80 : Publish a container's port(s) to the host i.e 
redirect all traffic coming to port 80 to container traffic

```
```sh
create a file named index.html in /home/ec2-user/html/ and 
copy the content from the attached index.html

```
### Testing
```sh
Access the URL http://your-host-ip-address/ using any browser
or curl http://your-host-ip-address/

You can use internal ip of the container
get the internal ip using 

docker inspect ee13d71edb10 | grep "IPAddress"

use this ip for curl command like below
curl 172.17.0.2

```