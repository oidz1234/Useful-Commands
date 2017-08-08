*Commands that I would not otherwise use/remember* 

*will eventually format this with fancy hyperlinks and the like*



**General commands**


	sudo !! (run last command as root (!! means to run the last command))

	pkill -9 -f “program” (kill all instances of a program)
	
	Source .bashrc (enable the updated bashrc)
	
	dpkg -l (list packages installed (debian based))



**Status commands**

	uname -a (show kernel version etc)

	less (pipe commands to this for easy reading (ls -la | less)

	df -h (drive information)

	free (memory information)

	ps -ef (list processes.)

	lsof (list open files)
	
	lsof -i:"portnum" (list services running on port)

	ps aux (current processes, aux flags = a - processs for all users, u - display process owner, x - 	show processes not attached to terminal)
	
	smartctl -a /dev/sda (lists abundence of information relating to hardrive health
	
	
**user commands**
	
	usermod -aG wheel *username* (add user to the wheel group)
	
	
**DD**

*data duplicatior(destroyer)*

the if and of stand for input file and output file

	dd if=/dev/sda of=/dev/sdb (clone one hdd to another hdd)
	dd if=/dev/sda4 of=~/hdadisk.img (backup of sda4 partition and name it hdadisk.img)
	dd if=hdadisk.img of=/dev/sdb3 (restore from .img file to dev/sdb3)
	
	



**Rsync**


	rsync -a ~/dir1 username@remote_host:destination_directory ( synch to a remote host (push))

	rsync -a username@remote_host:/home/username/dir1 place_to_sync_on_local_machine ( sync 
	from remote to local (pull))

**Screen commands**


	"ctrl a"  is the modifyer so screen knows a command is coming

	screen (start screen)

	screen -r  (reattach screen)

	ctrl ac  (move between screens)

	ctrl ak (kill current screen)

	ctrl aw (list screens)

	ctrl an (new screens)

	ctrl ad (detatch back to shell)

	ctrl a[ (enters copy mode (enter once to copy and enter again to save it to clipboard))

	ctrl a] (paste what is copied)

	ctrl a,  a  (send commands to nested screen) 

	ctrl a, | - split the session (ctrl a tab to switch between them)

	ctrl a, S – splits the session differnetly

	screen -X -S SCREENID kill (kill attached screen session)

	screen -D -r  (reconnect to attached screen session)


**Vi**


	dd  (delete line)

	dw (delete word)

	p  (put last deleted line)
	
	:w !sudo tee %  (save readonly file not opended as root)
	
	
**iptables**
	
*ip6tables for ipv6*
	
	iptables -t filter -A INPUT -s x.x.x.x -j REJECT (block the specified ip.) 
	
	-t table to use -A append -s source ip -j block method(REJECT, DROP).
	

**Git**
*soon (tm)*

**XTerm**

	shift insert (copy/paste)


**fail2ban**

	fail2ban-client status set <jailname (sshdisdefault)> unbanip x.x.x.x (unbans target ip)
	
**Tar**
	
	Tar -xzf ((e)xtract ze file!)
	Tar -czf (compress ze file!)
	
	
**ssh**
	
	$ ssh -L 9000:imgur.com:80 user@example.com (ssh tunneling (localhost:portnum(9000) to vist site))
	
**ss**

*replaces netstat*

	ss (shows all tcp,udp and unix socket information)
	ss -l (show current listing sockets)
	ss -t -u -x (these flags are for showing tcp,udp and unix connections)
	ss -a (need to add to show listing sockets as well. Default is only established connections)
	ss dst x.x.x.x (show how you are connecting to an ip)
	
**tcpdump**
	
	tcpdump not port 443 (show packets that do not come from 443. This can be done with mutiple ports as well)
	tcpdump - "interface" (show packets from that a certain interface)
	tcpdump "protocol" (show only certain protocol. see /etc/protocols for a list
	
**docker**

	docker pull "image" (download docker images)
	docker images (list all images downloaded)
	docker start "image id" (stat image in background)
	docker attach "image id" (reattach docker image to the terminal)
    docker run "image" (run a docker image. This creates a new container which you then need to save by commiting it.)
	docker run -it "image" (run a docker image and access the shell)
	docker commit -m "message" -a "author" "container-id" "repo/name" (commit a new docker image)
	docker commit "containerid" "repo/name" (simplier docker commit)
	docker ps -l (list containerid)
	docker ps (list all running containers)
	docker ps -a (list all containers)
	docker stop "container-id" (stop a running container)
	docker rmi "image" (remove docker image)
	
	
	
**Misc**

	python -m SimpleHTTPServer [port] (start a webserver serving the current directory)
	
	python -m http.server [port] (python3 of the above command)
	
	echo -n foobar | sha256sum (generate sha256 hash if "foobar" -n stops echo producing a trailing newline)
	
	badblocks -v /dev/sda (show badblocks on drive)
	
	pygmentize (cat with syntax highlighting)
	
	
	
