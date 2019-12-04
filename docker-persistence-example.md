# Data Persistence Example - Using Jenkins Image

```sh
docker run -p 8080:8080 -p 50000:50000 jenkins

and access the url using 

http://[docker-host-ip]:8080/ and configure using the initial password from the console screen
and create a sample test job

*initial password is also available in the below directory
cat jenkins/secrets/initialAdminPassword

now, stop the container and re-run the above command. You lost all your data!
You need to re-configure again.

To persit your data, use persistent volumes. Jenkins will store all the data under
/var/jenkins_home. Map this to your local folder.

docker run -p 8080:8080 -p 50000:50000 -v /your/home:/var/jenkins_home jenkins

and configure admin account and create some test jobs

docker stop and rerun using the above command

All youe created jobs are exists!
```

