## Install In Docker

```bash
$ git clone https://github.com/wazuh/wazuh-docker.git -b v4.14.6

$ cd wazuh-docker/multi-node/

$ docker compose -f generate-indexer-certs.yml run --rm generator

$ docker compose up -d
```

UserName : admin
Password : SecretPassword
