## Setting up Github!

- [ ] 1. Log into GitHub on your browser, and navigate to [https://github.com/ankithakannad/BridgeUP_Climate_Guardians_GitHub](https://github.com/ankithakannad/BridgeUP_Climate_Guardians_GitHub). This is my **remote repository**.

### Fork repository

- [ ] 2. Navigate to the right side of the window and click on &quot;Fork&quot;. This will save a new copy of the repository to your own GitHub account.

![fork a repo](https://github.com/amnh/BridgeUP-STEM-Oceans-Six/blob/master/photos/fork.png)

You can tell you're in your forked repository because the name of the repository will also have a description of where it was forked from. 

![forked from](https://github.com/ankithakannad/BridgeUP_Climate_Guardians_GitHub/blob/main/Guides/images/GitHub_guide_1.png)

- [ ] 3. Open up Terminal and navigate to your Desktop. 

Useful terminal commands:
   * **cd path/folder_name** navigates to a folder
   * **ls** shows all the files in your folder/directory.
   * **cd ..** moves you up one folder
   * **cd** (without anything after it) takes you to your home directory 
 
 - [ ] 4. Once you're in the right location, download your forked repository using **git clone \<url\>**, where **\<url\>** is the URL of your forked repository.
    * To find this URL, go to your GitHub account, open the repositories tab, find the forked repository, and click on the green button on the right side that says, \"Clone or download.\" Copy the URL it gives you.
    
  ![clone url](https://github.com/ankithakannad/BridgeUP_Climate_Guardians_GitHub/blob/main/Guides/images/GitHub_guide_2.png)
 
 ### Connect to Ankitha's repository
 
  - [ ] 5. Now, you've connected your remote (forked) repository with your local repository. GitHub gives this remote repository a nickname: **origin**. 
  
  - [ ] 6. Check that your forked repository is called origin by typing in **git remote -v** (**-v** or **-verbose** is simply asking **git** to list out the URL in addition to the names of the remote connections).  
  
  - [ ] 7. Now, let's connect to my repository so you can add in any new changes I've made to your local repository. We're going to call my repository **ankitha_repo**.
    * Type **git remote add ankitha_repo** **https://github.com/ankithakannad/BridgeUP_Climate_Guardians_GitHub** on Terminal.
    * Now, type **git remote -v** again. You should see two remotes: One called **origin** that points to your own repository, and one called **ankitha_repo** that points to mine.
    * If you make a mistake, type in **git remote set_url ankitha_repo \<url\>** to reset the URL.

- [ ] 8. Add me as a collaborator to your repository — that way, I'll be able to see your work and integrate it into the main repository. Go to "Settings" in your repository, visit "Collaborators" and add my username (ankithakannad) into the "Add collaborators" box. 

### Downloading and uploading files

- [ ] 9. Let's edit and add our first file to the repository. I'm going to add a .txt file for you to fill out in the "about_me" folder on GitHub. First, you'll have to pull the changes from my updated repository (**ankitha_repo**) onto your computer. 
    * In Terminal, type in **git pull ankitha_repo main**. **main** is the main branch of your repository. 

#### Without branching

- [ ] 10. Navigate to the "Labs" folder on your computer and open the "21_01_07_about_me.txt" file on Sublime. Answer the prompts provided.

- [ ] 11. When you're ready to upload your changes,
    * Type **git add .** to let GitHub know that you've made changes to your repository. Here, **.** means all the changes you've made. If only want to add a particular file, you would use the file name instead.
    * Type **git commit -m** \"\<Your message here\>\". Change \[Your message here\] to explain why you&#39;re making the change – i.e. &quot;Adding in my name&quot; etc. This lets GitHub know that your changes are ready to be uploaded.
	* To make sure the changes have been made, type in **git status**. If your commits have been uploaded, it should say &quot;Your branch is up to date with 'origin/main' &quot; (the **main** branch of your repository).

- [ ] 12. Next, you&#39;ll upload this change to your remote repository. Type **git push origin main**. This tells git to send the changes you made on the **main** branch of your repository to your forked repository on GitHub.

#### With branching

- [ ] 10. On GitHub, you can make new branches or copies of your repository to edit files without worrying about messing up your original repository. 
    * Create a new branch called edit_branch with **git branch edit_branch**
    * Switch to this branch using **git checkout edit_branch**
    * Navigate to the "Labs" folder on your computer and open the "21_01_07_about_me.txt" file on Sublime. Answer the prompts provided. 

- [ ] 11. When you're ready to upload your changes,
    * Type **git add .** to let GitHub know that you've made changes to your repository. Here, **.** means all the changes you've made. If only want to add a particular file, you would use the file name instead.
    * Type **git commit -m** \"\<Your message here\>\". Change \[Your message here\] to explain why you&#39;re making the change – i.e. &quot;Adding in my name&quot; etc. This lets GitHub know that your changes are ready to be uploaded.

- [ ] 12. Now you've informed GitHub of the changes you've made to the **edit_branch**. We need to merge these changes with your **main** repository.
    * Switch back to your main branch using **git checkout main**
    * Merge the changes you made in **edit_branch** to your **main** branch using **git merge edit_branch**.
    * Delete your branch using **git branch -d edit_branch**
    * To make sure the changes have been made, type in **git status**. If your commits have been uploaded, it should say &quot;Your branch is up to date with 'origin/main' &quot; (the **main** branch of your repository).
    
- [ ] 13. Next, you&#39;ll upload this change to your remote repository. Type **git push origin main**. This tells git to send the changes you made on the **main** branch of your repository to your forked repository on GitHub.

Congratulations! You just successfully pulled a file from an online repository, and pushed your changes back all using Terminal! You are a GitHub master in the making :sunglasses:
