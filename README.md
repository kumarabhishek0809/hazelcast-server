# hazelcast-server
hazelcast-server


Start 3 Members means 3 Instances of Hazelcast

--Add 3 clustered members
docker run --name hazelcast-5701 -p 5701:5701 hazelcast/hazelcast
docker run --name hazelcast-5702 -p 5702:5701 hazelcast/hazelcast
docker run --name hazelcast-5703 -p 5703:5701 hazelcast/hazelcast
docker run -d --name hazelcast-mgmt -p 38080:38080 hazelcast/management-center:latest

Then start management server
Use command docker inspect to know the management IP and Port
http://localhost:38080/hazelcast-mancenter/

docker run --name hazelcastManager -p hazelcast/management-center:latest
http://localhost:32774/hazelcast-mancenter/login.html
https://stackoverflow.com/questions/20385973/how-do-you-programmatically-configure-hazelcast-for-the-multicast-discovery-mech

