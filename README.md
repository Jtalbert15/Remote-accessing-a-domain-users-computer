# Remote-accessing-a-domain-users-computer

<img width="280" alt="Screenshot 2024-06-16 at 11 35 27 AM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/7978d680-645b-4141-a0ca-a16aeac7832a">

<h1>Summary</h1>

 In this lab we will remotely access a users computer. We will do this using Remote Desktop Connection provided by Windows. We will check that we can communicate with the computer via the ping command in command line, We will then ensure both computers have their remote desktop services on both computers, and finally we will remote into the users machine.

 <h1>More About Remote Desktop Protocol</h1>

 In order to accomplish this task we will utilize TCP port 3389. TCP (Transmission Control Protocol) is a connection based protocol meaning we need to establish a connection before we can send data. Simply put we start a TCP data transfer with a "3 way handshake". First our computer needs to send out a request to connect, then the receiving machine needs to acknowledge the request by communicating back to the first machine, then finally the sending machine will notify the receiving machine that the data is on the way. 

<h1>Step 1) Finding the Machine we want to Connect to</h1>

To start we need to find out what the computers name is that we created so on our Windows Server VM we are going to navigate to Active Directory Users and Computers

<img width="637" alt="Screenshot 2024-05-24 at 10 15 51 AM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/8010010e-7fc4-4990-9b96-8a917806a510">

Double click and you should see the name of our computer

<img width="631" alt="Screenshot 2024-05-24 at 10 16 36 AM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/052e3ead-5fd3-4bbf-b76a-8adbb1626a1a">

<h1> Step 2) Communicating with the Machine via the ping command</h1>

Now before we remote into that computer lets first check that we can communicate with the computer.

<img width="638" alt="Screenshot 2024-05-24 at 10 17 31 AM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/0da10307-194f-4b32-92bd-9cb35a85c1ea">

Navigate to the search bar in the bottom left corner of the screen and search cmd. Then click on command prompt.

<img width="635" alt="Screenshot 2024-05-24 at 10 19 45 AM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/93834c46-7e00-403f-9c28-86ca58b0028b">

Type ping followed by the name of your computer on your domain

<img width="631" alt="Screenshot 2024-05-24 at 10 21 01 AM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/157250f9-8d16-42a0-935c-5c8f550cf41f">

If you were successful in sending over the data you should see something like you see above

If not  make sure your VM is turned on or you may have to change your firewall settings

<h1>Step 3)Enabling Remote Desktop Services on both Machines</h1>

Now in the bottom left search bar we want to enable remote desktop services. To do this we need to search for services

<img width="633" alt="Screenshot 2024-05-24 at 4 45 22 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/d9033eb3-dbac-47a2-90c0-78c23e42a237">

Find Remote Desktop Services and double click on it

<img width="636" alt="Screenshot 2024-05-24 at 4 45 53 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/abb2bdd9-c3c8-4310-b6a8-515bdff4ee59">


<img width="635" alt="Screenshot 2024-05-24 at 4 47 03 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/3006d208-b1be-4fc2-b5bd-f30c89839a9c">

Now we want to click start followed by OK.

Now we want to enable it on the users computer we can do that from our server client by navigating to the search bar and searching for computer management.

<img width="635" alt="Screenshot 2024-05-24 at 4 49 47 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/43c4a978-83f6-4142-b868-becebfe0796c">

Once there we are going to right click on Computer Management in the top left of the screen and click on Connect to another computer...

<img width="639" alt="Screenshot 2024-05-24 at 4 51 06 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/d83d349d-eea1-4e05-b742-4074ec161714">

Then we need to choose the computer we want to access 
<img width="627" alt="Screenshot 2024-05-24 at 4 51 46 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/7ac0dd6e-67a5-4fb5-9ce9-7080111b62dc">

Click OK

Double click on Services and Applications

<img width="636" alt="Screenshot 2024-05-24 at 4 53 04 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/cb612bd0-302f-4cb7-a81f-a11bf79a74c4">

Double click on Services 

<img width="631" alt="Screenshot 2024-05-24 at 4 53 34 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/8413f2cd-58f0-4aa0-b935-eae768b58d49">

Find Remote Desktop Services and enable it like we did on the domain

<img width="632" alt="Screenshot 2024-05-24 at 4 55 14 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/ce8dacc8-4479-4785-80f7-60a422179ec8">

<h1>Step 4) Remoting into the Machine</h1>

Now we can Remote into that users device. To do this navigate to the search bar and search remote desktop connection 

<img width="632" alt="Screenshot 2024-05-24 at 5 18 02 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/47474e0e-59f3-40bd-98d0-f16714b7005d">

Now enter the computers name that you want to remote into 

<img width="631" alt="Screenshot 2024-05-24 at 5 18 47 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/5fa54636-9fe4-4c38-805c-2f40524fd996">

Click Connect

<img width="634" alt="Screenshot 2024-05-24 at 5 19 22 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/90842443-20be-40fe-a84a-4b93ac1e6a05">

Log into your administrator account

<img width="637" alt="Screenshot 2024-05-24 at 5 20 26 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/6562e1c5-0658-429c-9091-c33fea88d2ef">

You will then be prompted with this screen  

<img width="640" alt="Screenshot 2024-05-24 at 5 20 56 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/5f4df082-fde1-46b8-ac78-44af5254d0ac">

Click Ok

On the users device you are connecting they will be prompted with the screen below letting them know that you are trying to remote in as shown below.

<img width="627" alt="Screenshot 2024-05-24 at 5 21 42 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/20ef3a6d-4800-4c45-93ac-2da504fd0704">


Now we are in remote control of our users VM

<img width="637" alt="Screenshot 2024-05-24 at 5 23 00 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/da790aca-f385-46ff-8a35-22b1875613c5">

To end the session you can click the X button at the top of the screen

<img width="632" alt="Screenshot 2024-05-24 at 5 25 06 PM" src="https://github.com/Jtalbert15/Remote-accessing-a-domain-users-computer/assets/66844406/beae01c9-e315-4ac1-82b5-5285aafa549c">

Click Ok and now the user can log back into their computer 

