# Install docker
- [Windows](https://docs.docker.com/desktop/setup/install/windows-install/)
- [Mac](https://docs.docker.com/desktop/setup/install/mac-install/)
- [Linux](https://docs.docker.com/desktop/setup/install/linux/)

# Building and running your application
docker build -t my-apache-app .
docker run --name my-apache-app -d -p 80:80 -t my-apache-app

# Viewing your web page
- Open a browser and enter localhost in the URL bar
- You should see your webpage

# Pushing your code to dockerhub
## Creating a dockerhub account and repository
- Create a dockerhub account: https://hub.docker.com
- Create a repository. Name it my-apache-app

## Generating a gpg key locally
[gpg --generate-key](https://docs.docker.com/desktop/setup/sign-in/)


## Generate a personal access token
- Generate a personal access token on dockerhub - save this.

- Generate GPG key
gpg --generate-key

- Initialize the key
pass init ID

- Login
docker login -u username
    - Paste the PAT

- docker push jmcarman/my-apache-app:latest

- Tag your local image
docker tag local-image:my-apache-app new-repo:my-apache-app

## Pushing your local docker file to dockerhub
- Push your local docker file to dockerhub
docker push jmcarman/my-apache-app

