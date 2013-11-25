
 command 'sh-copy-id' found, did you mean:
 Command 'ssh-copy-id' from package 'openssh-client' (main)
sh-copy-id: command not found
[9986 10:28:56]:~  > ssh-copy-id root@zebra.liip.ch
root@zebra.liip.ch's password:
Now try logging into the machine, with "ssh 'root@zebra.liip.ch'", and check in:

  ~/.ssh/authorized_keys

to make sure we haven't added extra keys that you weren't expecting.

[9987 10:29:07]:~  > vim .ssh/config
[9988 10:29:27]:~  > ssh zebra.liip.ch
Enter passphrase for key '/home/Jean-christophe/.ssh/id_rsa':
Linux liip2 2.6.32-5-vserver-amd64 #1 SMP Sun Sep 23 12:45:03 UTC 2012 x86_64
              _                  _
__/\__  _ __ (_)_ __   ___   ___| |__   __/\__
\    / | '_ \| | '_ \ / _ \ / __| '_ \  \    /
/_  _\ | | | | | | | |  __/| (__| | | | /_  _\
  \/   |_| |_|_|_| |_|\___(_)___|_| |_|   \/

Willkommen auf Ihrem neuen Server von Nine!
(Um diese Meldung abzuschalten, geben Sie folgenden Befehl ein: rm /etc/motd.tail)

Beachten Sie folgende Hinweise:
