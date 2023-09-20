## Started the enumeration by sending a random email address that do not exit on the database.

Request

![Pasted image 20230920214255](https://github.com/numaan911098/leadgenapp-bug-report/assets/50366430/32387d23-023f-4f70-9394-cfb87f1e0ca4)


Response

![Pasted image 20230920214551](https://github.com/numaan911098/leadgenapp-bug-report/assets/50366430/c39584de-8edb-4706-8979-88a7b28ddd98)


## sending email address that exits on the database.

Request

![Pasted image 20230920214839](https://github.com/numaan911098/leadgenapp-bug-report/assets/50366430/28777cc6-961e-4d54-a263-8dd86cb382ae)


Response

![Pasted image 20230920214919](https://github.com/numaan911098/leadgenapp-bug-report/assets/50366430/9ed7c6eb-a08f-4e50-908b-5536163340e2)


#### In other applications this would have been a low finding but bcz of the week password policy(the application do not check for password strength and accept any string  > 8 characters). This can lead to a huge vulnerability. This is just a development server with limited accounts but on the main app there are thousands of accounts with week passwords an attacker can narrow down the potential users and can launch a huge scale Brute force attack .

### POC(Proof of concept)

now to exploit this vuln. I wrote a script that will take username wordlist as input just to keep it simple i didn't use any common username wordlist i created a wordlist from the users in slack example ["andleeb@leadgenapp.io", "aiman@leadgenapp.io","admin@leadgenapp.io"]. with these user emails i made use of the regex to search for "invalid_login_credentials" if this string exits in the response it means the user exits.

i will demonstrate this attack on a virtual lab.  so that it wont harm the real application bcz fuzzing can be really destructive. 
