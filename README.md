# Remote-accessing-a-domain-users-computer
In this lab we will remotely access a users computer

In previous labs we have created a Windows Server VM and a Windows 10 VM. Now We are going to remotely access our windows 10 computer.

To start we need to find out what the computers name is that we created so on our Windows Server VM we are going to navigate to Active Directory Users and Computers

<img width="637" alt="Screenshot 2024-05-24 at 10 15 51 AM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/8010010e-7fc4-4990-9b96-8a917806a510">

Double click and you should see the name of our computer

<img width="631" alt="Screenshot 2024-05-24 at 10 16 36 AM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/052e3ead-5fd3-4bbf-b76a-8adbb1626a1a">

Now before we remote into that computer lets first check that we can communicate with the computer.

<img width="638" alt="Screenshot 2024-05-24 at 10 17 31 AM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/0da10307-194f-4b32-92bd-9cb35a85c1ea">

Navigate to the search bar in the bottom left corner of the screen and search cmd. Then click on command prompt.

<img width="635" alt="Screenshot 2024-05-24 at 10 19 45 AM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/93834c46-7e00-403f-9c28-86ca58b0028b">

Type ping followed by the name of your computer on your domain

<img width="631" alt="Screenshot 2024-05-24 at 10 21 01 AM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/157250f9-8d16-42a0-935c-5c8f550cf41f">

If you were successful in sending over the data you should see something like you see above

If not  make sure your VM is turned on or you may have to change your firewall settings


