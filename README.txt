 
Task 7: 

 Monitor System Resources Using Netdata


 Objective:

 Install Netdata using Docker and visualize real-time metrics.

 Tools:

- Netdata
- Docker
- PowerShell


  Steps to Deploy Netdata:

1. Make sure Docker is installed and running on your system.

2. Open PowerShell or Git Bash.

3. Run the following command to deploy Netdata using Docker:

   docker run -d --name=netdata -p 19999:19999 --cap-add=SYS_PTRACE --security-opt apparmor=unconfined netdata/netdata

4. Once the container is running, open your browser and go to:

   http://localhost:19999

5. You should now see a live dashboard with detailed system metrics.

6. Logs can be explored in the Netdata container at /var/log/netdata

7. To stop Netdata: docker stop netdata

8. To remove it: docker rm netdata



 What Netdata Monitors:

- CPU usage
- Memory (RAM) usage
- Disk I/O (read/write activity)
- Network traffic
- Docker container stats
- System services and processes

 Dashboard:

 The live web interface where all metrics are visualized in real time. Accessible at: http://localhost:19999


  Key Performance Indicators (KPIs) to Monitor:

- CPU usage percentage
- Memory consumption
- Load average
- Disk read/write speeds
- Network upload/download rates
- Docker container performance


 Outcome:

 We now have a lightweight monitoring setup using Netdata that helps visualize and keep track of system and container performance in real time.


  Access:
  http://localhost:19999

  Monitors:
- CPU, Memory, Disk
- Docker containers
- Network traffic
- Processes

 Dashboard:
 Live, web-based charts (updates every second)
 

