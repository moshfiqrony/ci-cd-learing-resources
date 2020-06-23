## How to setup AWS for CodeDeploy
Base tutorial - [Automating your Delivery Pipeline from GitHub to Amazon EC2 using Jenkins | The Laboratory](https://www.youtube.com/watch?v=LFkGtg-ZTko&list=PLpIbMOwId_Uw13vAvc8Zl42PB_IgCCRwv&index=4&t=394s)
1. **Create EC2 instance**
2. **Instal awscli**
```
sudo apt install awscli
```
3. **Now configure AWS**
```
aws configure
```
    it will ask for these
      - AWS Access Key ID [None]
      - AWS Secret Access Key [None]
      - Default region name [None]
      - Default output format [None] - **leave this empty**
  
3. **Install aws codeDeploy agent**

Base Blog - https://docs.aws.amazon.com/codedeploy/latest/userguide/codedeploy-agent-operations-install-ubuntu.html
```
sudo apt-get update
sudo apt-get install ruby
sudo apt-get install wget
sudo wget https://aws-codedeploy-us-east-2.s3.us-east-2.amazonaws.com/latest/install
chmod +x ./install
sudo ./install auto
sudo service codedeploy-agent start
sudo service codedeploy-agent status
```
