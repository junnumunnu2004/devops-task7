
# Task 7 – Monitor System Resources Using Netdata

## Steps followed:
1. Created AWS EC2 Ubuntu instance
2. Installed Docker
3. Pulled and ran Netdata container:
4. docker run -d --name=netdata -p 19999:19999
-v /etc/passwd:/host/etc/passwd:ro
-v /etc/group:/host/etc/group:ro
-v /proc:/host/proc:ro
-v /sys:/host/sys:ro
-v /var/run/docker.sock:/var/run/docker.sock:ro
--restart unless-stopped netdata/netdata
4. Accessed dashboard via http://<EC2-IP>:19999
5. Verified metrics for CPU, RAM, and Docker containers.

## Screenshots:
- netdata_dashboard.png – dashboard view
- docker_ps.png – running container list

## Verification:
- `docker ps`
- `docker logs netdata`
git add .
git commit -m "Task 7 Netdata monitoring complete"
git branch -M main
git remote add origin https://github.com/<your-username>/task7-netdata.git
git push -u origin main
