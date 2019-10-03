## First steps

1. Run npm install after cloning repo down.
2. This is from a scotch-io tutorial. References to all code can be found here. 

https://scotch.io/tutorials/build-a-real-time-search-engine-with-node-vue-and-elasticsearch

3. These steps helped with installing and getting elasticsearch up and running on a mac OSX environment using node

## Installing Elasticsearch and getting up and running.
        1. Download Elasticsearch for Mac https://www.elastic.co/downloads/elasticsearch
        2. Double click to unpack
        3. Move folder to where you would like it or leave it in downloads
        4. If you leave the folder in downloads cd into downloads
        5. cd into the elastic search dir it will look something like elasticsearch-7-4.0
        6. Run ./bin/elasticsearch to start server
        7. Curl ‘http://localhost:9200' to test if server is running
        8. End elasticsearch process pkill -f elasticsearch

## Important things to be aware of
Every time you kill elasticsearch you will need to re rereun node data.js to add indices and data back into the server.

After you have installed elasticsearch you will need to change cors. To change this you will need to navigate into the config folder and then open then elasticsearch.yml using nano or vim and add

http.cors.enabled : true
http.cors.allow-origin : "*"

as instructed in the tutorial.

Example on how to open a text editor in the terminal if this is something new to you.

EXAMPLE: nano elasticsearch.yml

You can then head to the bottom of the file and add: 

http.cors.enabled : true
http.cors.allow-origin : "*"

## Repo run down

This is one of the few good examples I could piece together using a vue front end with elasticsearch. If you find this I hope it helps. It was confusing even with the help of a good tutorial. After playing with things it becomes a lot more clear what is doing what and the many relationships that are being made. Elasticsearch is incredibly powerful and I'm excited to use it more.






