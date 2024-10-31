**Some Assembly Required 1**

**There are no hints for this challenge**

Navigating to the URL displays a page that requires flag as the input. wierd, right ?

![Screenshot from 2024-10-31 16-00-11](https://github.com/user-attachments/assets/53930912-ec59-4191-87cb-19e8c05cdf46)

We will first inspect the source code using CTRL+u to see if there are any leads.  

![Screenshot from 2024-10-31 16-10-36](https://github.com/user-attachments/assets/2dd21c10-9750-40d8-adf4-b47999a2fc08)

We should check the contents of the javascript file.

![Screenshot from 2024-10-31 16-15-22](https://github.com/user-attachments/assets/b2b3f0ae-e020-4a82-ae3c-565101a273c7)

Some obfuscated js right there !

We will use developer tools to make the js more readable.

![Screenshot from 2024-10-31 16-18-42](https://github.com/user-attachments/assets/089998b6-9f8a-4079-bf9d-f9f23846ff72)

The code is more readable and it contains some wierdly named variables. There are no great leads in there.

We will use the network tab in web developer tools to see everything that the page loads.

![someassembly1](https://github.com/user-attachments/assets/51201707-509a-452f-8801-88434384649a)

There is an octet stream that we should check out. Double click the file and save it somewhere. We will then check the file type and read its contents.

![Screenshot from 2024-10-31 16-28-31](https://github.com/user-attachments/assets/02e683a6-fff7-45ba-87d1-0a6148c2158b)

The file is a webAssembly binary module, the file contains the flag at the bottom ):

![Screenshot from 2024-10-31 16-27-27](https://github.com/user-attachments/assets/3b14686a-570a-4dac-bde2-9e658d316956)
