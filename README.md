# Dynamic DNS Cloudflare Ansible Role

This roles sets up https://github.com/kshcherban/ddns-cloudflare 

Supported on x86_64 and arm64 Linux only.

It installs binary into `/usr/local/bin/ddns-cloudflare`, sets up cronjob for root user and logrotate to rotate logs.

Following variables can be set:

- **ddns_cloudflare_version** - version of binary, default `0.1.0`
- **ddns_cloudflare_schedule** - cron frequency in minutes, default `*/5`
- **ddns_cloudflare_token** - Cloudflare token to manage DNS, **required**
- **ddns_cloudflare_domain** - domain record that will be used, **required**
- **ddns_cloudflare_log** - log location, default `/var/log/ddns-cloudflare.log`