# Insomnia HTTP Client 

Welcome to the documentation site for [Insomnia](http://insomnia.rest). 
Insomnia is a beautiful cross-platform application for organizing, running, and 
debugging HTTP requests.

![Screenshot of Insomnia HTTP Client](/images/promo.png)


## Backstory and History

I first started on Insomnia in January of 2015. I was working at the SaaS startup 
[Sendwithus](https://www.sendwithus.com) which provides an API to send transactional emails. Before
I made Insomnia, I used [`curl`](https://curl.haxx.se/) to test the API features I was working on.
It was too painful to type in new commands for every endpoint I wanted to test, so I eventually
ended up with a folder full of scripts that I would call to do various things. Here is what my
folder might have looked like.

```
curl-commands/
 ├── send-email.sh
 ├── send-email-bad-data.sh
 ├── update-customer.sh
 ├── ...
 └── create-email-template.sh
```

It was messy. If I wanted to change the API key I was using I would have to either update it in
every script, or factor it out into an environment variable and soft-reference it. I knew there had
to be a better way. 

I forget how, but I stumbled upon the world of _REST Clients_. These were (usually) poorly written
web apps that allowed you to create and save HTTP requests. So, I tried them. All of them. And,
after a few days, realized that I didn't like any of them. So I started writing my own.

This is what the first (usable) version of Insomnia looked like.

![First version of Insomnia Chrome](/images/first-version.png)
