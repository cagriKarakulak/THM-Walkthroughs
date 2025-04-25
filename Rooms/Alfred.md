![953f1e4a27c7e04130b824ec1bc8e159](https://github.com/user-attachments/assets/37b709ff-5655-4a97-a2ad-7cd333807d2e)

https://tryhackme.com/room/alfred

# Alfred Walkthrough

## TASK 1 - Initial Access

How many ports are open? (TCP only)

-sS: Perform a SYN scan (stealth scan).

-sV: Attempt to determine the service/version running on open ports.

-Pn: Skip the ping scan; treat the host as online.

![qewq](https://github.com/user-attachments/assets/e7f5f5d7-c48f-4188-9b1b-f094fc56232a)

(3)

What is the username and password for the login panel? (in the format username:password)

You first need to download the Powershell script and make it available for the server to download. You can do this by creating an http server with python: python3 -m http.server

(No answer needed)

What is the user.txt flag? 

## TASK 2 - Switching Shells

What is the final size of the exe payload that you generated?

(73802)

## TASK 3 - Privilege Escalation

View all the privileges using whoami /priv

(No answer needed)

Enter: load incognito to load the incognito module in Metasploit. Please note that you may need to use the use incognito command if the previous command doesn't work. Also, ensure that your Metasploit is up to date.

(No answer needed)

Use the impersonate_token "BUILTIN\Administrators" command to impersonate the Administrators' token. What is the output when you run the getuid command?

(NT AUTHORITY\SYSTEM)

Ensure that you migrate to a process with correct permissions (the above question's answer). The safest process to pick is the services.exe process. First, use the ps command to view processes and find the PID of the services.exe process. Migrate to this process using the command migrate PID-OF-PROCESS

(No answer needed)

Read the root.txt file located at C:\Windows\System32\config

(dff0f748678f280250f25a45b8046b4a)
