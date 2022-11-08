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

1. Create a new job and give it an appropriate name 
2.  For `general` do the same as job 1
3.  For `Office 365 Connector` do the same as job 1
4.  For `Source Code Management` do the same as job 1 but then tick `Additional Behaviours` and click `Merge Before build`
    1.  `origin` as name
    2.  `main` as branch to merge to
5. For `build triggers` tick `Build after other projects are built` then pick job 1
6. For `Build Environment` do the same as job 1
7. Add a `Post-build Actions` click `Git Publisher`
   1. Tick `Push Only If Build Succeeds`
   2. Tick `Merge Results`
   3. Add branch
      1. `main` as branch
      2. `origin` as target
8. Click save
9. Make a change in the dev branch


### Job 3