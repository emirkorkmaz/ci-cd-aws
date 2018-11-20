This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).  
Deployment will be automated with TravisCI and occur on AWS  

Travis will be listening commits to master  
Upon commit, Travis will use .travis.yml file   
1st it will build the container by using Dockerfile.dev - this is because we want to execute tests. the same will be typed in "before_install"  
2nd Travis will execute tests by using the command given at "script"  
3rd Travis will deploy to AWS EBS by using Dockerfile dev. this will be handled by "deploy" command. EBS will recognize and use Dockerfile (not .dev, the prod instead) itself  

Another good things....  
In case you have created a pull request, travis will recognize it and start pre-checks. Unless these checks are passed, you cant merge the PR  

and...dont forget to use [skip ci] on commit messages for files to be ignore for triggering travis from build&deploy  

![1](https://github.com/emirkorkmaz/cloudera-quickstart-docker-compose/blob/master/misc/images/1.png "1")  
![2](https://github.com/emirkorkmaz/cloudera-quickstart-docker-compose/blob/master/misc/images/2.png "2")  
![3](https://github.com/emirkorkmaz/cloudera-quickstart-docker-compose/blob/master/misc/images/3.png "3")  
![4](https://github.com/emirkorkmaz/cloudera-quickstart-docker-compose/blob/master/misc/images/4.png "4")  
![5](https://github.com/emirkorkmaz/cloudera-quickstart-docker-compose/blob/master/misc/images/5.png "5")  
![6](https://github.com/emirkorkmaz/cloudera-quickstart-docker-compose/blob/master/misc/images/6.png "6")  
![7](https://github.com/emirkorkmaz/cloudera-quickstart-docker-compose/blob/master/misc/images/7.png "7")  
