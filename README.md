## Hello Spring Boot

This hello world Web app is created solely for learning/testing [Travis CI](https://travis-ci.org/).

The `.travis.yml` file contains two global environment variables, `DOCKER_USER` and `DOCKER_PASS`, that are used to 
login to [Docker Hub](https://hub.docker.com/) to push the created Docker image. These variables (after the `secure:` 
key) should be generated using the `travis` tool, as follows.

1. Install `travis` tool (some dependencies might needed to be installed beforehand):

        sudo gem install travis
        
2. Run the following commands from the project's root directory:

        travis encrypt DOCKER_USER="dockerhub_username"
        travis encrypt DOCKER_PASS="dockerhub_password"
    Copy the output values to `.travis.yml` file (i.e. `secure:` keys)