# docker-arm-swarm-monitor
Root repo for monitoring cluster of raspberry pi.

## Using it
Git clone the repo and use the given docker-compose.yml file. Delploy the full stack using the command

    docker stack deploy --compose-file docker-compose.yml monitoring

Grafana is exposed in localhost:3000 by default. Credentials are admin/admin. Make sure to change them if you want your work to be safe.

After getting done with the setup use a built in dashboard provided in the dashboard folder or check grafana's website.

The services takes some time to deploy so wait for a while. You can check the status of the services by 

    docker service ps 
    
All the global services needs to be replicated once in all the nodes and the others will have one instance in the swarm.
