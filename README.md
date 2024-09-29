# SIEM
The main goal of this project is to create a system that can watch for security events on my system. 

I did this by following this article by Christopher Elce : https://medium.com/@christoff.elce/setting-up-a-home-lab-for-elastic-siem-a-step-by-step-guide-e85f3750eb25

So First of All you have to sign up for a account at elastic.com 
Followin that your are prompted to create a depolyment ( This is the big overarching system that will be monitoring and tracking everything ) 

From there we install the Defend Instance which allows us to keep track of all the diffrent events that are taking place. Now because we are doing this through a VM set up the agrent on our VM and ultimatly then it was time to staet creating some secuirty events. 

I did this by running an NMAP scan. 

But really any process running can be searched and filtered for. 

Once the NMAP scan had run it was time to see if the SIEM had picked up all the logs and it diffenitly did

by using the process.args:"nmap" command I was able to seach for all times that that command had been used and and Endpoint log had apppeared. 

Using this the last step was to show it in a visual fassion as no one understands randong logs. 

So we went to the visualise section and added in a new visualization. well of how many records there as regarding the NMAP search. 

I did this by having a vertical bar graph our horizontial axies set to @timestap (To show when new records are being added) on our veritcal access is where I made it a count of all nmap log create activities. by using the same process.args:"nmap" 
![image](https://github.com/user-attachments/assets/925b6fc9-3d32-42b2-8459-7fe2be18b028)


Obviosuly this is a very simple idea however there can be so much more you can do with this like looking for incomming endpoint scans having that on a heatmap where you can see the events comming in from around the world. 


I think I am going to implment this in a future project I am thinking of doing where we create a honepot managethe traffic and visualize all the incomming requests from this heatmap dashboard. 
