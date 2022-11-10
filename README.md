#ansible
#server configuration
                                                      
1.	Launched three ec2 instances of ubuntu in AWS. One for ansible control node and other two are for the nodes in order to configure these nodes through this ansible control nodes by playbooks to configure apache server and display message on these two nodes and also to un deploy the apache server from 2 nodes.
	
  
  ![image](https://user-images.githubusercontent.com/59603371/201196982-56412e75-6cdf-4b16-9d41-27fdaa01f459.png)

1.a) ansible control node and other nodes configured in git bash.


![image](https://user-images.githubusercontent.com/59603371/201197124-099cc582-b26e-40c2-9743-2c4b8c771476.png)

	 
2.	Created new authentication key pairs for automating logins node1 and node2.


![image](https://user-images.githubusercontent.com/59603371/201197171-65b2efb1-bc80-4ba9-8c36-09da26711dfc.png)


 

3.	Created playbook for configuring apache using ansible on ubuntu yml file for installing apache2 server in nodes 1 and 2 through ansible control node. Apt line installs the apache2 and ensures we have updated_cache=yes.
 

![image](https://user-images.githubusercontent.com/59603371/201197234-b26bf817-f257-4d55-8098-591b69a706d8.png)


4.	Apache server was deployed in the 2 nodes as changed status is 1 and also got apache2 ubuntu default page when visited servers ip address on browser.
	

![image](https://user-images.githubusercontent.com/59603371/201197276-bc2c6ad7-515d-448d-b822-637bad531b64.png)

 

5.	Configuring apache modules for copying index.html page to /var/www/html path using ansible built in. copy on both nodes which displays message on browser when visited by their host names and apache server by default listening to port 8080.;

	 
   ![image](https://user-images.githubusercontent.com/59603371/201197314-51c675e4-40ae-4e7f-af7a-b32f55ee0bd0.png)


6.	Output after copying the html files to both nodes. 

![image](https://user-images.githubusercontent.com/59603371/201197358-40cdff38-fc7d-4a6b-abb7-3502de360fe1.png)


7.	Index.html page on node 1 which changes to SJSU 1 using lineinfile updating xvar to 1.

 ![image](https://user-images.githubusercontent.com/59603371/201197422-25772d47-8ca2-4bc2-b183-402697ce4bb6.png)

	

8.	Index.html page on node 2 which changes to SJSU 2 using lineinfile updating xvar to 2.

 
 ![image](https://user-images.githubusercontent.com/59603371/201197475-0732e114-b155-4b9a-9e56-e29a0609303b.png)



	
9.	Created playbook to un install the apache server on both nodes by using ansible playbook.


![image](https://user-images.githubusercontent.com/59603371/201197522-0b1df0ef-3d98-42e9-9fc8-0f37d418c745.png)


 


10.	Output after apache server is uninstalled.


![image](https://user-images.githubusercontent.com/59603371/201197569-a142ba3f-1b0a-4b85-b30a-317b46c57e10.png)


 

