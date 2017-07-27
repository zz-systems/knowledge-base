# Docker

## OSX GUI applications

### Setup
- install docker
- install XQuartz: `brew cask install xquartz`
- install socat: `brew install socat`

### Run
- Terminal 1:
	- Setup port forwarding: `socat TCP-LISTEN:6000,reuseaddr,fork UNIX-CLIENT:\"$DISPLAY\"` this blocks the terminal.
- Terminal 2: 
	- Allow remote IP on xhost: `xhost + $ip` 
where ip = ip address of vm. This has to be done on every system startup.
	- Start xserver: `open -a XQuartz`
	- Run application: `docker run -d --name firefox -e DISPLAY=$ip:0 -v /tmp/.X11-unix:/tmp/.X11-unix jess/firefox`


