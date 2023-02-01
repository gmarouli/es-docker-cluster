# es-docker-cluster
This projects sets up a docker compose file that sets up a cluster with:
- 2 dedicated elasticsearch master nodes (`es01` & `es02`)
- 2 dedicated elasticsearch data nodes ( `03` & `04`)
- 1 kibana

## How it works
1. Set-up a password at `.env`
2. Run `docker compose up` and wait :)
3. Access kibana at `localhost:5601` and use as username `elastic` and password you have set.

If you want to modify and rerun it but it looks like the previous state is causing troubles, clean up the containers and the volumes.
If this is the only thing you are running in docker you can use:
1. `docker compose down`
2. `docker volume rm $(docker volume ls -q)` (this will remove everything so be careful)
