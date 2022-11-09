![Alt text](/images/Jobthree.png)

rsync -avz -e "ssh -o StrictHostKeyChecking=no" app ubuntu@ec2-34-243-96-228.eu-west-1.compute.amazonaws.com:/home/ubuntu
ssh -A -o "StrictHostKeyChecking=no" ubuntu@ec2-34-243-96-228.eu-west-1.compute.amazonaws.com << EOF

cd app
nohup node app.js > /dev/null 2>&1 &
sudo killall -9 node

EOF
