# Stack files for Docker Cloud

A list of ready to use stack files to power your favorite services on Docker Cloud.

## Setup

### SSH Keys

Add your ssh keys to all your servers with a single file.
Replace "your_public_ssh_key" with your SSH public-key.
You can copy your key by pasting `pbcopy < ~/.ssh/id_rsa.pub` in your terminal.

[Stack file](authorized-keys.yml)

### Reverse Proxy + SSL

Enable a reverse proxy and SSL certifications from Let's Encrypt.
Now you can add domain names and secure connections to your Docker services.
Add envrionment variables like this to your services:
```yaml
environment:
    - LETSENCRYPT_EMAIL=your_email_address
    - LETSENCRYPT_HOST=your_domain_name
    - VIRTUAL_HOST=your_domain_name
```

[Stack file](reverse-proxy.yml)


## Monitoring

### Netdata

To configure Slack alerts get your webhook URL. [More infos here](https://www.programmableweb.com/news/how-to-integrate-webhooks-slack-api/how-to/2015/10/20)

[Stack file](monitoring-netdata.yml)

### cAdvisor

[Stack file](monitoring-cadvisor.yml)


## WordPress

### WordPress + MariaDB

[Stack file](wordpress-mariadb.yml)