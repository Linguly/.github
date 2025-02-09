# How to host Linguly from scratch

Here we are trying to document a step-by-step guid to self host a Linguly instance using [Coolify](https://coolify.io/).
It doesn't mean that this is the only way to host it but only a recommendation and guide to make it easier.

## 1- Where to run?

First step is to decide if you want to run it on an own system/running locally or deploy it on a server you own to access it easier from everywhere.

For the first option you can follow the local setup guides to run each app locally.

However, in this guide we are focusing on running them on a server using Coolify.

If you don't own a server, you can get a VPS (Virtual Private Server) from one of the well known providers such as:

- [Contabo](https://contabo.com/desktop/DE/en/vps/)
- [Hostinger](https://www.hostinger.de/vps)
- [Ultahost](https://ultahost.com/vps-hosting)

Minimum of 4 vCPU, 6GB RAM, 50GB Storage should be generally enough.

At the end, all we need here to continue to next steps is an IP and root password of the VPS server to do SSH.

## 2- Setup Coolify

Follow the quick installation from Coolify to install it in your server:
- https://coolify.io/docs/installation
- if you need further help for the firewall setup you can follow [this guide](./firewall-setup.md)
- after the installation is done you can follow the steps [in this video](https://www.youtube.com/watch?v=taJlPG82Ucw&t=232s) to setup the domain for your Coolify instance

- add Linguly's [Telegram Interface](https://github.com/Linguly/telegram-interface) and [Linguly Core](https://github.com/Linguly/linguly-core) using [the Github app integration](https://youtu.be/taJlPG82Ucw?feature=shared&t=1898) or just clone the latest 
    - configure the `BOT_TOKEN` and `LINGULY_CORE_BASE_URL` for the telegram interface using the environment variable
    > **NOTE**: `LINGULY_CORE_BASE_URL` can be your Linguly Core container name plus the exposed port e.g. `http://<coolify random name for the service>-<docker uuid>:3001`
    ![](./images/container-name.png)
    ![](./images/environment-variables.png)

## 3- Setup an LLM Model

...