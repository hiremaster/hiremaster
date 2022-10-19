# Website Deployment

## Deploy flask application to Elastic Beanstalk

```python

# Below contains example codes
# the path must be changed to your own enviroment

```

## Prerequisties

- Install EB CLI

  ```console
  pip install awsebcli --upgrade --user
  pip uninstall awsebcli
  export PATH=/Users/libosun/.local/bin/:$PATH
  eb --version
  ```

- Link: https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create-deploy-python-flask.html

## Set up a Python virtual environment with Flask

- Create a project directory.
  ```console
  ~$ mkdir eb-flask
  ~$ cd eb-flask
  ```
- Create and activate a virtual environment named virt:
  ```console
  ~/eb-flask$ virtualenv virt
  ~$ source virt/bin/activate
  (virt) ~/eb-flask$
  ```
- Install Falsk with pip install:
  ```console
  (virt)~/eb-flask$ pip install flask
  ```
- Save the output from pip freeze to a file named requirements.txt.
  ```console
  (virt)~/eb-flask$ pip freeze > requirements.txt
  ```

## Deploy your site with the EB CLI

- add .ebignore: Example ~/eb-flask/.ebignore
  ```console
  virt
  ```
- Initialize your EB CLI repository with the eb init command:
  ```console
  ~/eb-flask$ eb init -p python-3.7 flask-tutorial --region us-east-2
  Application flask-tutorial has been created.
  ```
- (optional) Run eb init again to configure a default keypair so that you can connect to the EC2 instance running your application with SSH:
  ```console
  ~/eb-flask$ eb init
  Do you want to set up SSH for your instances?
  (y/n): y
  Select a keypair.
  1) my-keypair
  2) [ Create new KeyPair ]
  ```
- Create an environment and deploy your application to it with eb create:
  ```console
  ~/eb-flask$ eb create flask-env
  ```

## Check back and Update

- open the link:
  ```console
  ~/eb-flask$ eb open
  ```
- update version:
  ```console
  eb deploy
  ```

## Eb PATH(Example):

```console
export PATH=/Users/libosun/.local/bin/:$PATH
```
