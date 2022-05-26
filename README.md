# Semantic-Search-Elasticsearch-Flask-Docker-
Built Semantic search and normal keyword search. For Semantic search model used is Universal Sentence Encoder(USE4). Deployed using flask. Built it in Docker.
![image](https://user-images.githubusercontent.com/87763217/170395167-c34db81d-adfb-4458-9063-5dbf7a72518d.png)

Commands used:
CMD:
* docker run -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" --name newmyelastic docker.elastic.co/elasticsearch/elasticsearch:8.2.0
* docker exec -it -u 0 newmyelastic bash
* docker cp archive.zip newmyelastic:/usr/share/elasticsearch/searchqa/
* docker cp searchES_FlaskAPI.py newmyelastic:/usr/share/elasticsearch/searchqa/
* docker cp universal-sentence-encoder_4.tar.gz newmyelastic:/usr/share/elasticsearch/searchqa/data/


Docker:
* apt-get update && \ apt-get -y install sudo
* sudo apt-get install -y python3
* sudo apt-get install -y python3-pip
* sudo apt-get install -y vim
* sudo apt-get -y install wget
* sudo apt-get clean all
* sudo python3 -m pip install --upgrade pip
* sudo python3 -m pip --version
* sudo python3 -m pip install elasticsearch
* sudo python3 -m pip install pandas
* sudo python3 -m pip install --upgrade --no-cache-dir tensorflow
* sudo python3 -m pip install --upgrade tensorflow-hub
* sudo apt-get install –y tar
* tar -xvzf universal-sentence-encoder_4.tar.gz -C ./USE4

* sudo python3 -m pip install flask
* LC_ALL=en_US
* export LC_ALL
* export FLASK_APP=searchES_FlaskAPI.py
* python3 -m flask run
* curl http://127.0.0.1:5000/search/how+to+install+python
