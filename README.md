The goal here is to demonstrate github codespaces as a potential lab environment for training. 

If you came here for some other purpose this should be working code written in node.js 

to append to a stream and to read from a stream

It requires an eventstoredb docker container running single node with no authentication

This needs to run in a container with docker in docker enabled. 

Then the student would need to run this command, in the future I may load this automatically

The -d runs it in the background. 

docker run -d --name esdb-node -it -p 2113:2113 -p 1113:1113 \
    eventstore/eventstore:latest --insecure --run-projections=All \
    --enable-external-tcp --enable-atom-pub-over-http
