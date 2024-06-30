## WEB GAUNTLET
### 1)
Its based on SQL injection. We know that our username for access is admin/adminstrator.However we dont have the password. So we have to make the statement terminate at our username such that the password we input does not matter.  
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/91bc4ed0-d9e2-4c7f-9344-a35a5c923a4c)  
We have multiple ways to ensure that our password input is ignored. One such way is using semicolon which maarks the end of statement so anything beyond it is not read.(When only one statement is executed).  
This method works in stage 1-3.
However in stage 4 we cant use the word 'admin'. So we have to input it so it concatenates using "||" operator.  
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/2154abed-b560-4eb9-8b6f-86634679ca94)  
This same method can be used in stage 4 and 5.  

Clearin stage 4 and 5 gives a script on .php page which contains flag : picoCTF{y0u_m4d3_1t_16f769e719ab9d3e310fd13dc1262ee1}  

### 2)web gauntlet 2
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/942097df-5a27-4f07-bd52-cd80a796e3db)  

  Here we cant use the ; operator.  
So instead we can use the IS NOT operator.  
As in this challenege we have to enter a password we pass an IS NOT statement which is true in password. As its true we pass.  

![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/f8736d26-6c6a-4f8d-b03e-2e81196edf45)    
Flag is : picoCTF{0n3_m0r3_t1m3_fc0f841ee8e0d3e1f479f1a01a617ebb}

### 3)WEB GAUNTLET 3

The method we used in previous challenge satisfies the conditions of this challenge too so we use the same method.  

![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/942097df-5a27-4f07-bd52-cd80a796e3db)  

( Here we cant use the ; operator.  
So instead we can use the IS NOT operator.  
As in this challenege we have to enter a password we pass an IS NOT statement which is true in password. As its true we pass.  )

![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/40dc0d4f-330a-42b8-adeb-95dccd46dcb7)   
Flag is: picoCTF{k3ep_1t_sh0rt_30593712914d76105748604617f4006a}

### 4)Irish-name-repo 1

In this challenge our previous method of making our password be ignored works again.  
We have a menu panel in top left where we click on admin login.  
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/5c725560-edcb-4d0a-8bd6-5d6b67ec9bfd)  


We again use ' to end username input and then semicolon to stop statement reading.
Here too password does not matter.




![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/b8808488-d05d-4935-928b-871d17c58834)

### 5)Irish-Name-Repo  2
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/e54a785c-15c7-41c0-9453-11d0f7f77c24)

Our previous method is still working.
We again use ' to end username input and then semicolon to stop statement reading.
Here too password does not matter.  

![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/824268e0-30fb-4cc7-a9e4-558e76781644)  

### 6)Irish-Name-repo 3  
This time none of our previous methods work as this time we can input only password.  
I tried to input an or statement such that we have a random string or 1=1 -- however this didnt work.(-- is used to comment out)  

So instead we open site on burp suite and intercept when we enter a random password.  
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/27f9642d-4e2b-4b9c-98ec-bf7229e11a67)

We see that in last line debug=0. On turning debug to 1, we see that our random paassword is changed and then used . We can see that the change is quite obvious all input letters are rotated by 13 places or encrypted in ROT13.  
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/edaa56a4-06ee-4102-88df-a4600ddbfaaa)  
As our or statement was getting encrypted it was not working however we can now rotate it and make it work.   
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/f3efd715-9f4d-4df8-a494-604ac636fcdd)  
We only need to rotate or to be as numerals are not rotated.We got the flag.  

### 7) JaWT Scratchpad
The hint tells us about the jwt cookie. So after logging in randomly we check cookies and get the jwt cookie.  
I used burp suite and got the jwt cookie from the response.  
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/54fea564-c2e7-4e82-a9e7-8ff86d019868)  
On exploring we find the cookie is made of 3 main constituents:  
1)Header: Gives type of cookie and type of hash.  
2)Payload: Gives user.
3)Verification: Has secret sign.  

As we have the jwt cookie we can use John The ripper To get the password.  
We get the secret sign as:ilovepico  
Now we input secret sign and change user to admin .  
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/f1e0a064-ab1d-4e4d-a367-d77489cd06e8)

We use this new generated cookie and replace the old jwt cookie and refresh the page.  
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/80466f2d-81f9-414b-b73f-ffed7d052cb8)


![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/6be14964-51a6-4445-b675-a6057f5579ab)  

### 8)Secrets  
Our hint is folders. On inspecting the page in sources we see a secret folder. So we add secret/ to link and enter.  
Now we see a further hidden folder in it. We now add hidden/ to link and enter.  
Again we see superhidden/ which on adding to link and entering we see .   
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/ee5df92b-6c59-43d7-a0fc-52a5bcf59f8d)

![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/fb16c10e-abee-41e1-995a-b00cee5203ac)
However flag is visible in our inspect panel.  
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/c788fcd7-354d-4adb-ba25-2db98610cc7f)

### 9)Client-side-again  
We see a password panel on our link. However as i cant find anything interesting with it i open the inspect panel and on opening it i straight away see an html script in which further a java script is hidden.  
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/aa9cd789-9bd2-4346-aa8c-ffa8e4557873)  

![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/d9da7318-c8c7-4351-ae91-b4ee7548d804)  

![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/755615a9-0367-4fe7-b7d1-166bd037127d)  

![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/db0c5924-0581-485e-8109-48b51f87da10)  
The java scipt has a _0x4b5b variable . On determining its values we can get: 
Flag substring characters :  
        0-8:  picoCTF{
        7-9:  {n
        8-16:  not_this
        3-6:  oCT
        24-32:  37115} '
        6-11:   F{not
        16-24:  _again_3
        12-16: this   
        
  Remove overlapping characters to get flag: picoCTF{not_this_again_337115}  

### 9)  

        










![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/35b5e6c3-e886-4bec-982b-fef733ecf451)


![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/06d96dd9-8a3d-4891-8c70-56dbddc8b1d8)























![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/2200364d-5971-458d-972d-863e06707671)


![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/403c6d2d-f5bd-4b1e-bf21-0dd3ccd31940)




![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/12d8c1ee-3acf-4b6f-ab4d-93e37871e7a6)


![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/aed21727-a51f-4889-b280-b056ca652016)





