After Configuration Suricata adn also install the agent on the server of wazuh

- Changed the File

```bash
# Changed this Config File
$ sudo vim /var/ossec/etc/ossec.conf

# Changed the Content
    <localfile>
        <log_format> json </log_format>
        <location> /var/log/suricata/eve/json</location>
    </localfile>

```
