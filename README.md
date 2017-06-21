*Commands that I would not otherwise use/remember* 



**General commands**


	sudo !! (run last command as root (!! means to run the last command))

	pygmentize (cat with syntax highlighting)

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

	ps aux (current processes, aux flags = a - processs for all users, u - display process owner, x - 	show processes not attached to terminal)





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
	
**Misc**

	python -m SimpleHTTPServer [port] (start a webserver serving the current directory)
	
	python -m http.server [port] (python3 of the above command)
	
	echo -n foobar | sha256sum (generate sha256 hash if "foobar" -n stops echo producing a trailing newline)
	
	
