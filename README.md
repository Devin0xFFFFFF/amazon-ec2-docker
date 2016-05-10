# amazon-ec2-docker

###Instructions for setting up Docker and Docker Compose on an EC2 Instance

##Instructions

- Create a new Amazon Linux Instance
- SSH into your new instance
- Run 'sudo yum update -y'
- Run 'sudo yum install -y docker'
- Run 'sudo service docker start'
- Run 'sudo usermod -a -G docker ec2-user'
- Log out and log back in again to pick up the new docker group permissions
- Run 'sudo curl -L https://github.com/docker/compose/releases/download/1.4.0/docker-compose-`uname -s`-`uname -m` | sudo tee /usr/local/bin/docker-compose > /dev/null'
- Run 'sudo chmod +x /usr/local/bin/docker-compose'
- Start using Docker!

##Resources

- [Running Docker/Docker-Compose on AWS](http://blogs.sourceallies.com/2015/05/vagrantfile-docker-compose-dockerrun-aws-json/)
- [Setting up Docker/Docker-Compose on AWS](http://www.mattkimber.co.uk/setting-up-docker-and-docker-compose-on-aws/)
- [AWS Docs for Docker Basics](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/docker-basics.html)
- [Docker Setup JSON](https://gist.github.com/hitsujiwool/81fcab49f9ccf8ac5835)
