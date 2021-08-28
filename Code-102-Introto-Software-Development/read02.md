# GIT
is a DVCS that stores data in a file system made up of snapshots. Each time you save a changed version of your project — called commit — Git creates a snapshot of the file and stores a reference to it. If the file has not changed, Git only stores a reference to the already-stored identical version of it.
 ***Git use somthing called (vc) and (lvc):***
### Version Control(vc):
*Version Control is a system that allows you to revisit various versions of a file or set of files by recording changes. Through version control, one can revert a file or project to a previous version, track modifications and modifying individuals, and compare changes. By utilizing a Version Control System (VCS), mistakes with files can easily be rectified.*
### Local Version Control (lvc):
Many years ago, programmers created Local Version Control systems. A Local VCS entails one database on your hard disk that stores changes to files.
### Benefits of **GIT** to programmers:
1. Local Operations:  
because most necessary information can be found in local resourcesThis allows for process expediency because a project's history resides on the local disk, eliminating the need to fetch history information from the server, and allowing one to continue work on a project even when not online or on a VPN.
2. stoting data and changes:  
Git is set up to greatly minimize the possibility of irreversible damage to files, such as accidentally lost data. Git makes it extremely difficult for a snapshot of your file that is committed to be lost.

3. Tracking Changes:  
Every single change applied to any file or directory is tracked by Git. And, as the gatekeeper, Git will always detect file corruption or loss of information in transit.  


## 1. (ACP) : How GIT Tracking
* adding file  
  1. git add (file name)  
  2. git add .    ( for all files)  
* Committing a File  
  1. git commit -m “made change x,y,z (for multiple files)  
  2. git commit -a (Committing All Changes) 
* Pushing Changes  
  1. git push origin master
* git status : that command allows you to see the information   




## 2. clone is a way to connect between GIT and GitHub to share or upload your work or download it in your local machine . 

## some of anothe command in ***GIT**:

command|what do 
-------|-------
LS    | list the files and folders 
 mkdir|create new folder
    cd|change Dir having a where i am
 touch|make a new file
   pwd|print current dirit's show's me where i'm
 cd ..|going back one folder 
  cd ~| to home dir
git branch -d test|for Deleting Branches

![git image](https://hackernoon.com/hn-images/1*QoR3rxWIbnf5wmF_IuAHqQ.png)
[for more information](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/#2_1)