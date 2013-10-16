Well I have some emails where the TO field is generated dynamically and it would also be nice to test that the TO field is being set correctly. Yes, I could set the TO field to my email address and put the dynamically created TO field in the message and then change it right before I send it live. But I'd rather not. I'm also buliding entire systems in development with many different pages sending emails. I don't want to have to make sure I fix them all before going live.

A solution could be to create my own mail() function like mymail() that automatically replaces the TO field with my email and puts the original TO, CC, and BCC into X-original-to, etc in the header. Unfortunately, I have thousands of pages out there already and I would like this to be a global thing.

I found a solution that would do what I'm looking for here:
[blog.phpdoc.info...]

It basically changes the sendmail_path line in php.ini to:
sendmail_path=/usr/local/bin/trapmail

Then you create the /usr/local/bin/trapmail file like so:
formail -R to X-original-to -R cc X-original-cc -R bcc X-original-bcc -f -A "To: devteam@example.com" ¦ /usr/sbin/sendmail -t -i

This uses the formail command to change the headers and sends it to sendmail.

Unfortunately, I still have some problem because it's still sending to the original to address. If I get it to work I'll share.

If anyone else gets it to work, please let me know. Thanks.
