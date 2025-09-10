# Configure-Windows-Group-Policy

## What is Group Policy?
**Group Policy is a Windows Server feature that allows administrators to set rules and manage settings for users and computers in a network.**

**👉 With Group Policy, an admin can:**

**Block or allow access to Control Panel**

**Enforce password policies (length, complexity, expiry)**

**Restrict or allow software installations**

**Set desktop wallpaper or system configurations for all users**

**In this project, I configured Group Policy in Windows Server to manage user restrictions. First, I created two users and applied a domain-level policy to block the Control Panel. Then, I created an Organizational Unit (Demo OU) and moved one user into it. Finally, I linked the Group Policy to the OU, ensuring the restriction was applied only to that specific user. This project demonstrates practical skills in Active Directory management, Group Policy configuration, and policy scoping.**

## Steps
**1:- First, I created two users in Active Directory to demonstrate this project.**
<img width="991" height="637" alt="1 (1)" src="https://github.com/user-attachments/assets/874779a9-3950-427d-9f4c-d30c28ca7d54" />

**2:- Next, I created an Organizational Unit, where I would later add a user and link the Group Policy.**
<img width="1001" height="317" alt="2 (1)" src="https://github.com/user-attachments/assets/b654c62f-20d0-4399-9ff7-5b9f4ff84a18" />

**3:- Now, I opened Group Policy Management to create a new Group Policy.**
<img width="1012" height="416" alt="3 (1)" src="https://github.com/user-attachments/assets/c7c781c3-37a6-4c43-86a5-b5996283c3de" />

**4:- Next, I right-clicked on the domain and created a new Group Policy, assigning it a name.**
<img width="907" height="500" alt="4 (1)" src="https://github.com/user-attachments/assets/c4f35467-e03f-4afa-9637-81593789fdcf" />

**5:- The newly created policy is now visible with its assigned name.**
<img width="883" height="308" alt="5 (1)" src="https://github.com/user-attachments/assets/df882dba-65e5-4e38-bd89-57e0c573e284" />

**6:- Now, right-click on the Group Policy that you created.**
<img width="1019" height="717" alt="6 (1)" src="https://github.com/user-attachments/assets/82aa8c8c-94a9-4276-aa85-a4c2d78226c4" />

**7:- Next, go to Administrative Templates and select Control Panel, as I will be blocking the Control Panel in this project.**
<img width="1002" height="714" alt="7 (1)" src="https://github.com/user-attachments/assets/b3218f6b-318e-4256-ad43-210f60bf8344" />

**8:- In the Control Panel settings, click on Prohibit access to Control Panel and PC settings**
<img width="1013" height="688" alt="8 (1)" src="https://github.com/user-attachments/assets/b42acec3-d6ca-4c0b-b35e-dfdf32aebd23" />

**9:- Now, enable the setting, click Apply, and then OK. Your policy is now configured.**
<img width="969" height="678" alt="9 (1)" src="https://github.com/user-attachments/assets/667db3ff-6da6-4e4f-901f-d2f915bc42eb" />

**10:- Now, update the policy by running the gpupdate command.**
<img width="981" height="488" alt="10 (1)" src="https://github.com/user-attachments/assets/453e5739-b6df-4c90-b19a-567121e0d3be" />

**11:- Now, when you try to open the Control Panel, it will be restricted because the policy is applied at the domain level. Next, we will apply it only to specific users.Here’s how we will do it.**
<img width="970" height="505" alt="11 (1)" src="https://github.com/user-attachments/assets/57e39661-ff3e-40e4-8e6c-62a00965f80e" />

**12:- Now, move the user into the Organizational Unit that we created in the beginning.**
<img width="997" height="674" alt="12" src="https://github.com/user-attachments/assets/badcfc77-85a0-4b67-b3ce-fa889760a222" />

**13:- In the Group Policy section, link the Group Policy to the Organizational Unit and remove the domain-level policy.**
<img width="1010" height="707" alt="13 (1)" src="https://github.com/user-attachments/assets/c45f5ccd-826b-4270-bd94-175c6d852ed5" />

**14:- You can now see that the policy is linked with the Organizational Unit.**
<img width="1012" height="408" alt="14 (1)" src="https://github.com/user-attachments/assets/41b6ced4-f2ec-4fa5-8665-b71db6ad45b0" />

**15:- Now, when you try to open the Control Panel, it will open normally. However, the user added to the Organizational Unit will be restricted from accessing the Control Panel.**
<img width="963" height="581" alt="15 (1)" src="https://github.com/user-attachments/assets/6aae39dd-d6aa-41dd-87d2-a2b82d21c6ff"


## 🔚 Conclusion

This project successfully demonstrates how Group Policy in Windows Server can be used to centrally manage and enforce security policies across users and computers in a domain environment.

By creating users, setting up an Organizational Unit (OU), and applying a Group Policy Object (GPO) to restrict Control Panel access, I showcased the ability to:

Enforce restrictions at the domain level for all users.

Narrow down the scope by linking policies to a specific Organizational Unit (OU), applying restrictions only to selected users.

Use policy updates (gpupdate) to apply changes in real time.

**Through this hands-on implementation, I gained practical skills in Active Directory management, policy scoping, and user-specific restrictions. This project highlights the importance of Group Policy in strengthening security, standardizing configurations, and ensuring better control within enterprise environments.**
















       
