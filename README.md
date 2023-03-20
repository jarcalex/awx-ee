# awx-ee

sudo apt install docker.io

pip install ansible-builder

export GITHUB_CRT_TOKEN=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

echo $GITHUB_CRT_TOKEN | docker login ghcr.io -u jarcalex --password-stdin

/home/ajarc/.local/bin/ansible-builder  build --tag ghcr.io/jarcalex/awx-ee:0.0.1 --container-runtime docker -f execution-environment.yml

docker push ghcr.io/jarcalex/awx-ee:0.0.1

