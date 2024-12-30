conda create -n px python=3.11 -y && conda activate px

pip install torch transformers accelerate huggingface_hub sentencepiece 

SearXNG:

git clone https://github.com/vaibhav-s-dabhade/searxng.git && cd searxng

under searx directory in settings.yml file, change following:

search:
  formats:
    - html
    - json

sudo chmod 666 /var/run/docker.sock 
make docker.build   

docker run --rm -d -p 32768:8080 -v "${PWD}/searxng:/etc/searxng" -e "BASE_URL=http://localhost:$PORT/" -e "INSTANCE_NAME=my-instance" vaibhav-s-dabhade/searxng

http://localhost:32768