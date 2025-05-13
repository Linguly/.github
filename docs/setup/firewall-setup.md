---
layout: default
permalink: /docs/setup/firewall-setup/
---

# Firewall Setup
## Configure Firewall Rules

To achieve the desired firewall rules, follow these steps:

1. **Allow SSH Traffic**

    Allow SSH traffic on port 22:
    ```sh
    sudo ufw allow 22/tcp
    ```

2. **Allow Application Ports for Coolify**

    Allow traffic on ports 6002, 6001, and 8000:
    ```sh
    sudo ufw allow 6002/tcp
    sudo ufw allow 6001/tcp
    sudo ufw allow 8000/tcp
    ```

    > **NOTE**: 8000 can be removed if you are using your domain to access the dashboard.

3. **If you want to use the domain to access the dashboard**
    Add 443 and 80 and remove 8000:
    ```sh
    sudo ufw allow 443/tcp
    sudo ufw allow 80/tcp
    sudo ufw delete allow 8000/tcp
    ```

3. **Enable the Firewall**

    Enable the firewall to apply the rules:
    ```sh
    sudo ufw enable
    ```

4. **Verify Firewall Status**

    Check the status to ensure the rules are correctly applied:
    ```sh
    sudo ufw status
    ```

The expected output should include:

```terminal
Status: active

To                         Action      From
--                         ------      ----
22/tcp                     ALLOW       Anywhere                  
6002/tcp                   ALLOW       Anywhere                  
6001/tcp                   ALLOW       Anywhere                  
443/tcp                    ALLOW       Anywhere                  
80/tcp                     ALLOW       Anywhere                  
22/tcp (v6)                ALLOW       Anywhere (v6)             
6002/tcp (v6)              ALLOW       Anywhere (v6)             
6001/tcp (v6)              ALLOW       Anywhere (v6)             
443/tcp (v6)               ALLOW       Anywhere (v6)             
80/tcp (v6)                ALLOW       Anywhere (v6)
```
