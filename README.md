# CTFd Registration Patch
Official CTFd Site: https://ctfd.io
Official CTFd Github: https://github.com/CTFd/

Adds registration code field to registration page as seen here:

<img src="https://raw.githubusercontent.com/cxp714/ctf-challs/master/CTFd-patches/register.png" alt="Registration Code" width="250"/>

Also removes the oauth login option from reg and login pages

### Replace these files in the Docker container:
- CTFd/auth.py
- CTFd/CTFd/themes/core/templates/register.html
- CTFd/CTFd/themes/core/templates/login.html

Replace qwerty in line 167 of the 'auth.py' file with whatever you want the registration code to be:

`reg_valid = regcode == "qwerty"`

If the code does not match the user gets an error, if it does they can register

Share the code to whoever you'd like to be a member. 
