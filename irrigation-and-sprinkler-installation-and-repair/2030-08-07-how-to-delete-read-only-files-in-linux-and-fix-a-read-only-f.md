---
title: "How to Delete Read-Only Files in Linux (and Fix a Read-Only File System Error)"
date: 2030-08-07 19:38
author: Marcus Chen
---

# How to Delete Read-Only Files in Linux (and Fix a "Read-Only File System" Error)

Skip to Content Quizzes PRO Courses Hot Guides  Tech Help Pro  Expert Videos  About wikiHow Pro  Upgrade  RANDOM EXPLORE

Tech Help ProAbout UsRandom ArticleQuizzes

Request a New ArticleCommunity DashboardTrendingForums

Arts and EntertainmentArtworkBooksMovies

Computers and ElectronicsComputersPhone SkillsTechnology Hacks

HealthMen's HealthMental HealthWomen's Health

RelationshipsDatingLoveRelationship Issues Hobbies and CraftsCraftsDrawingGames

Education & CommunicationCommunication SkillsPersonal DevelopmentStudying

Personal Care and StyleFashionHair CarePersonal Hygiene

QuizzesLove QuizzesPersonality QuizzesFun Games

Arts and EntertainmentFinance and BusinessHome and GardenRelationship Quizzes

Cars & Other VehiclesFood and EntertainingPersonal Care and StyleSports and Fitness

[to Delete](https://to-delete.northlist.xyz/to-delete/202608266006.html)

Computers and ElectronicsHealthPets and AnimalsTravel

Education & CommunicationHobbies and CraftsPhilosophy and ReligionWork World

Family LifeHolidays and TraditionsRelationshipsYouth LOG IN Log in

Social login does not work in incognito and private browsers. Please log in with your username or email to continue. Facebook Google wikiHow Account No account yet? Create an account Subscribe Home Random Browse Articles TrendingNew Quizzes & Games All QuizzesHot Love Quizzes Personality Quizzes Fun Games Dating Simulator Learn Something New Forums Courses Happiness Hub Explore More Support wikiHow About wikiHow Log in / Sign up Terms of Use

wikiHow is where trusted research and expert knowledge come together. Learn why people trust wikiHow Categories Computers and Electronics Operating Systems Linux How to Delete Read-Only Files in Linux Co-authored byStan Kats and Nicole Levine, MFA

Last Updated: March 16, 2026Fact Checked Changing File Permissions | Using sudo | Fixing the Read Only File System Error | Expert Interview |Show more|Show less X

This article was co-authored by Stan Kats and by wikiHow staff writer, Nicole Levine, MFA. Stan Kats is a Professional Technologist and the COO and Chief Technologist for The STG IT Consulting Group in West Hollywood, California. Stan provides comprehensive technology solutions to businesses through managed IT services, and for individuals through his consumer service business, Stan's Tech Garage. Stan holds a BA in International Relations from The University of Southern California. He began his career working in the Fortune 500 IT world. Stan founded his companies to offer an enterprise-level of expertise for small businesses and individuals. 

This article has been fact-checked, ensuring the accuracy of any cited facts and confirming the authority of its sources. 

This article has been viewed 164,923 times. 

If you want to delete a file that has read-only permissions in Linux, you have a few options. If the file belongs to you, you can either change the file's permissions or use the sudo command to delete the file as root. But if you're trying to delete a file that has write permissions and still can't delete it (or you see a "Read Only File System" error), you may need to remount the drive with proper permissions. We'll show you how to remove any read-only file on any Linux distribution, including Ubuntu and Linux Mint. Deleting a Read Only File in Linux

If it’s your file, give yourself write permissions by writing chmod -v u+rw filename. Then, you can delete the file. If you don’t own it, you can use sudo chmod -v u+rw filename to get permission, then use rm filename to delete the file. Steps Method 1 Method 1 of 3: Changing File Permissions 1

Open a terminal window. If a file you own is read-only, you won't be able to delete it unless you give yourself write permission for that file. If you're using a window manager, press Ctrl + Alt + T to open a terminal window now.[1]XResearch source

Use this method if you're trying to delete a file that belongs to you but (e.g., you're the owner or in a group that has access to read the file) but don't have permission to delete it.[2]XExpert SourceStan Kats

Professional TechnologistExpert Interview

If you're signed in remotely and already at a command prompt, just skip to the next step. 2

Use cd to enter the directory of the file you want to delete. For example, if the file you want to delete is inside a folder called documents in your home directory, you'd use cd documents or cd /home/username/documents. Advertisement 3

Use ls -al to display the file permissions for the files in the directory. Using ls -l displays a list of files in the directory, along with the owner of each file and its permissions.[3]XResearch source Adding the a to ls -l also shows hidden files and folders in the directory. 4

[and Fix Read-Only](https://and-fix-read-only.themaplelane.com/and-fix-read-only/20260826078.html)

Evaluate the permissions of the file you want to delete. The permissions for a file appear before its name like this: r--r--r--. The owner's name appears after it, followed by the group name.

r is read permissions, w is write permissions, and x is execute permissions.

The first three characters in the permissions (in this example, r--), are the file owner's permissions. So, in this example, the owner of the file only has read permissions, which means they can't write to, execute, or delete the file. [4]XResearch source

The second three characters are group permissions. If you're a member of a group and that group has write permissions to the file, you'll be able to delete it even if you're not the owner.

The third three characters are world permissions, which is everyone else. 5

Use chmod -v u+rw filename to give yourself read and write permissions. You can omit the r if you already have read permissions. Once you have write permissions, you'll be able to delete the file.

If you're not the file owner but have root access to the system, you can use sudo chmod -v u+rw filename to give yourself the right permissions.[5]XResearch source

To see the file's new permissions, run ls -al again. 6

Use rm filename to delete the file. Now that you have write permissions on the file, deleting it will be simple.[6]XResearch source

If you aren't able to delete the file after making it writable, its partition may be mounted read-only. See Fixing the Read Only File System Error to troubleshoot. Advertisement Method 2 Method 2 of 3: Using sudo 1

Open a terminal window. You can use the sudo command to delete a read-only file that you aren't able to delete with your user account. If you're using a window manager, press Ctrl + Alt + T to open a terminal window now.

Use this method if you are not the owner of the file you want to delete and you'd rather just delete the file instead of first changing its permissions.

If you're signed in remotely and already at a command prompt, just skip to the next step. 2

Use cd to enter the directory of the file you want to delete. For example, if the file you want to delete a file inside a folder called documents in your home directory, you'd use cd documents or cd /home/username/documents. 3

Use ls -al to view the contents of the directory. This command will display all of the files in the current directory, as well as each file's owner and permissions. 4

[Fix Read-Only File System](https://fix-read-only-file-system.themaplelane.com/fix-read-only-file-system/202608262399.html)

Use sudo rm filename to delete the file. You'll be prompted to enter your password to obtain root-level permissions.[7]XExpert SourceStan Kats

Professional TechnologistExpert Interview Once your password is accepted, the read-only file will be deleted.

If you aren't able to delete the file with sudo, its partition may be mounted read-only. See Fixing the Read Only File System Error to troubleshoot. Advertisement Method 3 Method 3 of 3: Fixing the Read Only File System Error 1

Open a terminal window. If you're trying to delete a file and getting an error that says rm: cannot remove '(filename)' : Read only file system, there are a few possible causes. Start by pressing Ctrl + Alt + T to open a terminal window if you're using a window manager.

[Files in Linux and](https://files-in-linux-and.themaplelane.com/files-in-linux-and/20260826.html)

If you're signed in remotely, just move to the next step. 2

Run df -h to view all mounted devices. You'll need to know the exact mount point of the drive that's giving you trouble. This displays all mounted drives.[8]XResearch source 3

[in Linux and Fix](https://in-linux-and-fix.northlist.xyz/in-linux-and-fix/202608266511.html)

[and Fix Read-Only](https://and-fix-read-only.swapstreet.shop/and-fix-read-only/202608269575.html)

Run the command mount . Replace mount point with the actual mount point, e.g., /media/usbdisk. If you're trying to delete a file on a removable disk or network drive, such as an old backup, the disk where the file is stored might be mounted as read-only.[9]XResearch source

If you see ro in the results, the file system is read-only. Remounting the drive should fix the error. To do so, use mount -o remount,rw mount point. You can then delete the file.

[Fix Read-Only File](https://fix-read-only-file.curblist.xyz/fix-read-only-file/20260826.html)

If the permissions are rw, the disk is mounted with read-write permissions, which means you should be able to delete files without problems. This usually means there's a problem with the file system on the drive. Continue with this method.

If you see remount-ro, this means the there's a problem with the file system and the drive was remounted as read-only to limit additional damage. This also means there's a problem with the file system on the drive. Continue with this method. 4

If the permissions are correct, unmount the drive. To do this, run sudo umount device.[10]XResearch source Replace device with the device name, e.g., /dev/sdd1.

Since you can't unmount a root file system, you can't check the file system of the root partition unless you're booted into recovery mode. If the error is on the root file system, boot into recovery mode first. 5

Run sudo fsck -n device to check the drive. This checks the integrity of the drive without making any changes. If the drive is okay, you'll see "clean" in the results. If there are errors, you will see them.

If there are errors, back up the drive before you continue in case the file system cannot be repaired. 6

Run sudo fsck device to repair errors. If there are errors, you'll be prompted to correct them.

[Read-Only File System Error](https://read-only-file-system-error.swapstreet.shop/read-only-file-system-error/20260826.html)

Even if you are able to correct errors, make a backup just in case the drive is dying. 7

Remount the drive once repaired. If you were able to repair the errors, remounting the drive will make it so you can delete your files. Use mount -o remount,rw mount point to ensure the drive is remounted with read and write permissions. You should then be able to modify and delete files on the drive.[11]XResearch source Advertisement Expert Q&A  Search Add New Question Ask a Question 200 characters left

Include your email address to get a message when this question is answered. Submit Advertisement Tips Submit a Tip 

All tip submissions are carefully reviewed before being published Name 

Please provide your name and last initial Submit Thanks for submitting a tip for review!  You Might Also Like

2 Simple Steps to Delete Read Only Files How to

Delete Locked Files on a Mac with Finder or Terminal How to

Fix the Zsh: Permission Denied Error on Mac How to

Delete a File or Folder Showing Error "Access Is Denied" How to

Change File Permissions in Linux from the Terminal How to Delete Files That Cannot Be Deleted How to Delete Corrupted Files on a PC or Mac How to

[Fix Read-Only File](https://fix-read-only-file.swapstreet.shop/fix-read-only-file/20260826.html)

Run a File in Linux: Terminal & GUI Methods A Guide to Disabling Write Protection How to Delete a File On Your Computer How to

Access and Use the Root Account in Linux

[Does WhatsApp Notify for Screenshots? Your Question Answered](https://github.com/t7glsei1ek/yrkfrs/blob/main/hot-tub-service-and-repair/2030-07-07-does-whatsapp-notify-for-screenshots-your-question-answered.md)

6 Easy Ways to Fix a USB Drive That is Stuck in Read-Only Mode Advertisement Expert Interview

Thanks for reading our article! If you'd like to learn more about Computer Networking, check out our in-depth interview with Stan Kats. References

↑https://www.youtube.com/watch?v=BmVmJi5dR9c

↑Stan Kats. Professional Technologist. Expert Interview

↑https://www.youtube.com/watch?v=BmVmJi5dR9c

↑https://www.youtube.com/watch?v=BmVmJi5dR9c

↑https://www.youtube.com/watch?v=BmVmJi5dR9c

↑https://www.ibm.com/docs/en/aix/7.2.0?topic=r-rm-command

↑Stan Kats. Professional Technologist. Expert Interview

↑https://oneuptime.com/blog/post/2026-01-24-read-only-file-system-errors/view

[and Fix Read-Only File](https://and-fix-read-only-file.curblist.xyz/and-fix-read-only-file/20260826.html)

↑https://oneuptime.com/blog/post/2026-01-24-read-only-file-system-errors/view More References (2)

↑https://oneuptime.com/blog/post/2026-01-24-read-only-file-system-errors/view

↑https://oneuptime.com/blog/post/2026-01-24-read-only-file-system-errors/view About This Article Co-authored by:  Stan Kats Professional Technologist

This article was co-authored by Stan Kats and by wikiHow staff writer, Nicole Levine, MFA. Stan Kats is a Professional Technologist and the COO and Chief Technologist for The STG IT Consulting Group in West Hollywood, California. Stan provides comprehensive technology solutions to businesses through managed IT services, and for individuals through his consumer service business, Stan's Tech Garage. Stan holds a BA in International Relations from The University of Southern California. He began his career working in the Fortune 500 IT world. Stan founded his companies to offer an enterprise-level of expertise for small businesses and individuals. This article has been viewed 164,923 times.  How helpful is this? Co-authors: 4 Updated: March 16, 2026 Views: 164,923 Categories: Linux In other languages Indonesian Portuguese French Hindi Vietnamese Thai Chinese Dutch Italian Spanish Japanese Print Send fan mail to authors

Thanks to all authors for creating a page that has been read 164,923 times. Is this article up to date? YesNo Advertisement

Cookies make wikiHow better. By continuing to use our site, you agree to our cookie policy. Co-authored by:  Stan Kats Professional Technologist Click a star to vote Co-authors: 4 Updated: March 16, 2026 Views: 164,923 Quizzes & Games What Tarot Card Am I Quiz Take Quiz

What Kind of Reality Check Do I Need Quiz Take Quiz The Impossible Quiz Take Quiz Taylor Swift Song Quiz Take Quiz You Might Also Like

2 Simple Steps to Delete Read Only Files How to

Delete Locked Files on a Mac with Finder or Terminal How to

Fix the Zsh: Permission Denied Error on Mac How to

Delete a File or Folder Showing Error "Access Is Denied" Trending Articles Am I Chopped Quiz Can We Guess How Tall You Are Quiz Kiss, Marry, Kill Quiz What’s the Name of My Crush? Trending Articles Finish the Lyrics TikTok Edition

Design a Morning Routine and Learn Your Superpower

Pick a Door and We'll Reveal What You're Missing What Kind of Doomed Am I? Take the Quiz. Face the Truth. 🔥 Am I Gay Quiz Do I Have a Type? Am I Hard to Love? Am I a Spoiled Brat? 🤔 Are You More... 🤔 How Tuff Am I? What Kind of Wolf Is My Personality?

Am I More Golden Retriever or Black Cat? Villain or Hero Quiz Featured Videos

The Right Way to Refrigerate and Freeze Fresh Green Beans

A Complete Guide to Shaving Your Body (and Preventing Razor Burn) How to

Play "What Are the Odds?" (Also Known As "Odds Are")

4 Easy Ways to Draw Cute and Realistic Cats Hot Takes Only 🔥 Overrated or Underrated Game

Do You Agree With These Spicy Hot Takes?

Do You Agree with These Hygiene Hot Takes?

Weird Would You Rather: What Do You Choose? Your Daily Dose of Fun 🎉

Do You Agree with These Popular Hot Takes?

Let Us Guess Your Age Based On Video Game Nostalgia Rizz Game: Test Your Rizz

Can You Pull Off The Perfect Heist? Prove Yourself Categories Computers and Electronics Operating Systems Linux

© 2026 wikiHow, Inc. All rights reserved. Use of site content is subject to our Terms of Use. wikiHow Tech Newsletter You're all set!

Helpful tech how-tos delivered to your inbox every week! Sign me up!

By signing up you are agreeing to receive emails according to our privacy policy. Home About wikiHow Experts Jobs Contact Us Site Map Terms of Use Privacy Policy Do Not Sell or Share My Info Not Selling Info Contribute Follow Us × wikiHow Tech Help:

Tech troubles got you down? We've got the tips you need Subscribe You're all set! X - - 662
