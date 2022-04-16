## Welcome to how add ssh key in GitHub and Windows

### *First... ¿What the fuck is ssh key?* :worried:

#### Definition by google:

SSH Key is a protocol security that allow to user connect with a server or differents servers without need be login with his user and password each time that need do some action in the server. :sleepy:

**¿Don't you have any idea what that mean?**

:rage: **...**

Okey this is my definition for noobs:

> " This is only a protocol safer that allow connect differents services/servers.  **EXAMPLE: YOUR ACCOUNT GITHUB** avoiding the typical login and without exposing your credentials, then you only need have your private ssh key in the place that you want to register ( :neutral_face: Yes, yes, your pc for example ) and share the public ssh key to service as in this case your Github Account, and with that form github know that key is your pc and you can clone your repositorys, do differents actions without need of 1000 configurations ( Okey no that's not true, the others forms are very easier too, but using the ssh key you can be more **PRO** :sunglasses: ) "

### So, ¿What are the steps to do for this configuration? :confounded:

**First, Windows (In this case Windows 10/11):**

1. You need install Git in your computer, https://git-scm.com/.

*this is not a tutorial for how install github :joy: so, if you don't know, go to google bro*

2. Open your git Bash ( this programm will be installed when you are installing git )

3. configuring git

    - **Global credentials config of git**
    - git config --global user.name "Your github name"
    - git config --global user.email "yourgithubemail@gmail.com"

**Finally what we came for :sob:**

We will config your ssh key in windows ( remember in this case version 10/11, *I dont know if others versions are the same xd* )

**1. In your git bash, run this command**
    
    - ssh-keygen

First, you will be asked about the location where the keys should be stored. By default, your user folder will contain a folder called .ssh. Leave it as it is and hit the Enter key.

*Note: if you dont have some specific location only press enter :cold_sweat:*

Next, you will be asked to set a password to protect your private key. Without a password, anyone obtaining your private key can impersonate you.

*Note: If you dont wanna write some password for this ssh key, only press enter*

*Note 2: Remember :joy: if you will write some password, when you're writing that is not visible but relax, you're writing.*

*Note 3: While it is a good practice to set a password, it is very hard in Windows to store that password in a way that you don’t have to type it every time you run a command in Git.*

Now you have generated yours public and private key :kissing:


**2. If you open the location that the key was created, ( *Remember first command, the first question is about the location, like this example in /c/Users/youruser/.ssh*)**

- there you can find the id_rsa ( private ssh key ) and id_rsa.pub ( public ssh key )

Now the last part :blush:

**3. Add your SSH key to GitHub**

- open the public ssh key, id_rsa.pub
    - for example using cat
    > cat /c/youruser/.ssh/id_rsa.pub

- copy all info in the file

**Finally go to your profile in github and go to setting => SSH or click link https://github.com/settings/ssh/new and add the info that you have in the public key** :dizzy_face:

Now you can clone your respositories using SSH in github.

**References:**

- Thanks to the Valentin Despa ( https://vdespa.medium.com/ ) all the information using here, was based in the next article of him  https://medium.com/devops-with-valentine/2021-how-to-set-up-your-ssh-key-for-github-on-windows-10-afe6e729a3c0