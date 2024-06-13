# cloudflare-ufw
Two-liner to update UFW to allow Cloudflare IPs! Requires curl and ufw to be installed.

In addition, these commands are recommended to be run:

    sudo ufw limit ssh
    sudo ufw allow from 192.168.0.0/24 comment 'HOME IP'
    sudo ufw default deny incoming

We don't block ssh outright since Cloudflare won't proxy ssh... And for self-hosters at home,
the second line helps with direct LAN access without external port forwarding and routing 
back and stuff :P

Inspiration from https://rietta.com/blog/using-iptables-to-require-cloudflare/
