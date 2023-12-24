## Remote Setup

### Install

    curl -L https://fly.io/install.sh | sh

### Provision

    fly launch --copy-config --vm-size shared-cpu-1x

"Do you want to tweak [...]"? Yes:

- Postgres: None

Create a 1GB volume so Fly won't create a 3GB one for us during deploy:

    fly volumes create data --size 1 -y -r gru

### Deploy

    fly deploy
