# CICD

![Alt text](/images/task.png)

### Job 1 steps 

1. Created a repo on github with the app folder inside 
2. I made a new ssh key pair using the ssh folder on my local host
3. I used `cat` to see the public key and pasted that into the settings of the github repo
4. I now needed to make a new job in Jenkins
5. I gave it an appropriate name `subhaan-CI` and then clicked `freestyle project` and then `ok`
6. Gave an appropriate description
7. Ticked `Discard old builds` and set `Max # of builds to keep` to `3`
8. Ticked `GitHub project` and then went onto my repo and copied the HTTPS link provided when clicking on the `Code` dropdown and pasted it into the prompt
9. In `Office 365 Connector` I Ticked `Restrict where this project can be run` and input `sparta-ubuntu-node` might need to backspace and click again to get it to work
10. In `Source Code Management` Tick `Git` and copy the ssh link from the same place you got the HTTPS link and paste it in. An error will appear but we will deal with this. 
11. Click on the `add key` symbol and a prompt should appear:
    1.  Change kind to `SSH Username with private key`
    2.  Add an appropriate username 
    3.  Tick `Enter Directly`
    4.  Paste in your private key
    5.  Click `Add`
12. find and click the credential you just made and the error should go
13. configure the branch. So I put it as `dev` as i made a new branch using `$ git checkout -b <branch-name> `
14. In `Build Triggers` tick `GitHub hook trigger for GITScm polling` 
    1.  To set up webhook go to the repo setting and on the left hand side click `webhooks`
    2.  copy Jenkins IP address and add `/github-webhook/` at the end of it
    3.  Click `save`
    4.  go back to Jenkins
15. In `Build Environment` tick `Provide Node & npm bin/ folder to PATH `
16. In `Build` add 
    ```bash
    cd app
    npm install
    npm test
    ```


### Job 2

git merge origin/dev
hello hello