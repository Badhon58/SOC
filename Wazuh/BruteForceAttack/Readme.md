# Brute Force Attack

## Requirements

Create **2 AWS EC2 instances** with **Amazon Linux**.

- **Web Server** – Hosts the SecureBank application
- **Wazuh Server** – Hosts the Wazuh SIEM

Install the following on both servers:

- Docker
- Docker Compose
  - ![Docker Compose Installation Link](./Docker.sh)
- Git

---

### Web-Server

Clone the SecureBank repository.

```bash
git clone https://github.com/ssrdio/SecureBank.git

# Navigate to the project directory.
cd SecureBank

# Modify the `docker-compose.yml` file if needed, then start the application.
docker compose up -d
```

Image:
![SecureBank Web Application](./Website.png)

---

## Wazuh Server Setup

Clone the Wazuh Docker repository.

```bash
$ git clone https://github.com/wazuh/wazuh-docker.git -b v4.14.6

# Navigate to the deployment directory.
$ cd wazuh-docker/multi-node

# Generate the required certificates.
$ docker compose -f generate-indexer-certs.yml run --rm generator

# Start the Wazuh services.
$ docker compose up -d

# UserName : admin
# Password : SecretPassword
```

If Not Working

```bash
$ sudo mkdir -p /root/.docker/cli-plugins

$ sudo cp ~/.docker/cli-plugins/docker-compose /root/.docker/cli-plugins/docker-compose

$ sudo chmod +x /root/.docker/cli-plugins/docker-compose

$ sudo docker compose version

$ sudo usermod -aG docker ec2-user

$ sudo docker compose -f generate-indexer-certs.yml run --rm generator
```

![Wazuh DashBoard](./WazuhDashboard.png)

---

Wazuh Agent Set Up
Note : The ip of that server address will be the wazuh dashboard

![Wazuh Agent Set Up](./Wazuh.png)

![After Install the Agent in the Application](./SecureBankEndpoint.png)

---

## Now Lets Perform Brute Force Attack

Set Up the brup Suite For Attack

- InterSecpet the traffic
  ![InterSecpet the traffic](./Set%20up%20the%20CRT.png)

- Live Traffic Capture
  ![Live Traffic Capture](./Click%20ON%20Login%20Button.png)
  ![Open the Traffic with Burp](./Open%20It%20with%20Burp%20Suite.png)
  - Send it to the Intruder

- Cluster Attack Using Brup Suite
  ![Cluster Attack On Brup Suite](./BurpSuiteAttacks.png)

- Check On the Threat Hunter
  ![Check On the Threat Hunter](./Wazuh%20BFAttack%20Monitor.png)
  ![BFA Event](./BFA%20Event1.png)

---

# Linux System Monitoring

## Action Creation & Manipulation