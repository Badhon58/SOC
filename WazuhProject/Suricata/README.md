- Install Suricata in Kali Linux

```bash
# Install in Kali Linux
$ sudo apt install suricata -y

# Reboot
$ reboot

# Enable Suricata
$ sudo systemctl enable suricata

# Start the Suricata
$ sudo systemctl start suricata

# Check The Status Suricata
$ sudo systemctl status suricata

# All the Configuration and rules are Stored
$ ls -al /etc/suricata

# To Config the suricata
$ sudo vim /etc/suricata/suricata.yaml

# Changed the ip or the private ip range in
vars:
    address-groups:
        HOME_NET : ["192.168.216.0/24"] # Check the range of the IP Address $ ip a (eth0)

# Now we need changed the af-packet
af-packet:
    - interface : eth0 # ifconfig

# Now If we want to changed the rule then we need to go /rule
rule-files:
    - suricata.rules
    - /path/local.rules

# Then UpDate Suricata
$ sudo suricata-update

# Check The Directory all the dependency
$ sudo ls -al /var/lib/suricata/rules

# Specifying Your Own Sources
$ sudo suricata-update list-sources

# Adding rules set to the configuration
$ sudo suricata-update enable-source <List-Name>
$ sudo suricata-update enable-source tgreen/hunting

# To Check the Source enable to the suricata
$ sudo suricata-update list-sources

# If any problem occur on the file Then simple
$ sudo suricata-update remove-source <source-name>

# Test the Configuration File
$ sudo suricata -T -c /etc/suricata/suricata.yaml -v

# ******* Important Restart Suricata **********
$ sudo systemctl restart suricata

# Start the Suricata Server
$ sudo systemctl start suricata.service

# Check the Suricata Server Status
$ sudo systemctl status suricata.service

# The log file of suricata server are in
$ sudo ls -al /var/log/suricata

# Check if the suricata IDS is Working or Not
$ curl http://testmynids.org/uid/index.html
$ sudo cat /var/log/suricata/fast.log


# sudo tcpdump -i eth0 icmp
```
