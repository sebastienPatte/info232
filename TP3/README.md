Instructions for TP3
========

This week you are (finally) working on your own project. 
If your group name is groupname (for instance doctor, or orbiter, etc.) then your group email is groupname@chalearn.org. It can be used to send email to all your group members, connect to your group Codalab account and your group Github account.

Steps 1 and 2 must be performed by your **group leader** only.

Table of Contents
=================
* [Step 1: Create group Codalab account and download the starting kit](#step-1-create-group-codalab-account-and-download-the-starting-kit)
* [Step 2: Create Group Github Account and a Group Repo](#step-2-create-group-github-account-and-a-group-repo)
* [Step 3: Clone the group repo](#step-3-clone-the-group-repo)
* [Step 4: Run the jupyter notebook](#step-4-run-the-jupyter-notebook)
* [Step 5: Submit the sample code to Codalab](#step-5-submit-the-sample-code-to-codalab)

## Step 1: Create group Codalab account and download the starting kit

* **Test Your Group Email:**

**GROUP LEADER:** Send a welcome message to all your group member asking them to reply, by sending email to groupname@chalearn.org. Check that everyone received the message (if they did not reply, investigate the problem, e.g. they should check in they spam box). In case of problem, ask your teacher.

* **Create a Group Account on Codalab:**

**GROUP LEADER:** Go to https://codalab.lri.fr/competitions/ and create a NEW account in the name of the group, using **groupname@chalearn.org as email and groupname as login**. Use info232 as password or share the password with all your group members.

* **Download the starting kit:**

GROUP LEADER:  Go to [your competitions](http://saclay.chalearn.org/) on Codalab (e.g. group DOCTOR goes to competition HADACA). Go to the "Participate" tab, click on "Files".
Download the starting kit by clicking on "Starking kit".

On your local computer, create a directory for your project 

(**replace `groupname` by your group name!!!**):
```bash
cd ~/projects
mkdir groupname; cd groupname
mkdir starting_kit; cd starting_kit
unzip ~/Téléchargements/starting_kit.zip
```

## Step 2: Create Group Github Account and a Group Repo

* **Initialize your local repo:**

**GROUP LEADER:**  On your local computer, initialize git:
```bash
cd ~/projects/groupname/
git init
git add starting_kit/
git commit -m "First commit"
```
* **Initialize your remote repo:**

**GROUP LEADER:**  Go to [https://github.com/](https://github.com/) and create a NEW account in the name of the group, using groupname@chalearn.org as email.

Create a new repo. Name it also groupname. Do NOT initialize it with README.

On your local computer, push the contents of the starting kit to the repo:

```bash
cd ~/projects/groupname/
git remote add origin https://github.com/groupname/groupname.git
git push -u origin master
```

## Step 3: Clone the group repo

**EVERYONE IN THE GROUP, EXCEPT THE GROUP LEADER:** Once your leader has created your github repo, you can all clone it on your computer.
**The group leader should not perform this step, because he/she has already a local version of the repo.**

```bash
cd ~/projects
git clone https://github.com/groupname/groupname.git
```


## Step 4: Run the jupyter notebook

**EVERYONE IN THE GROUP, INCLUDING THE GROUP LEADER:**

Fetch the `public_data/` from /partage. WARNING: replace challengename by your challenge name (e.g. if you are working on "areal" use `public_data_areal` instead of `public_data_challengename`).

```bash
cd ~/projects/groupname/
ln -s  /partage/public/isabelle.guyon/M2_AIC_2019/public_data_challengename public_data
```
This does not actually copy the data but it makes it available to you via a symbolic link.

Start a jupyter-notebook and run README.ipynb (for instructions to run from home, see [TP1 Appendix A] (https://github.com/zhengying-liu/info232/blob/master/TP1/README.md#appendix-a-how-to-access-the-jupyter-notebook-from-home). Otherwise:

```bash
cd ~/projects/groupname/starting_kit/
jupyter-notebook --ip=127.0.0.1 README.ipynb
```
Make sure you are running Python 3, otherwise see [TP1 Step3] (https://github.com/zhengying-liu/info232/blob/master/TP1/README.md#step-3-launch-jupyter-notebook-and-answer-questions-of-this-tp).
Run the jupyter notebook and run every cell to verify eveything works properly. 

At the end of the notebook you should see a message similar to:
```console
Submit one of these files:
../sample_code_submission_18-12-09-21-06.zip
../sample_result_submission_18-12-09-21-06.zip
```
REPLACE `sample_data` by `public_data` in the notebook then use the option Kernel > Restart & Run All to generate submissions using the dataset of the challenge NOT just the sample data.

## Step 5: Submit the sample code to Codalab

**GROUP LEADER ONLY:**  
Make sure you have re-run your notebook on the `public_data` (see last instruction of the previous step).
Go to the Codalab page of your competition (check [http://saclay.chalearn.org/](http://saclay.chalearn.org/)). Go to the "Participate" tab, click on "Submit / View Results", and submit one of the files that was generated by the notebook. After a few seconds, refresh the page and make sure that your score has successfully been computed and go to the "Results" tab to check your submission is recorded in the leaderboard. If yes, you have successfully made your first submission to your challenge!

Next: organize your group in 2 binomes (preprocessing, prediction, and visualization) and split the work to prepare the project proposal.

