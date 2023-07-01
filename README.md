wget -q -O aptos_dev.sh https://api.nodes.guru/aptos_dev.sh && chmod +x aptos_dev.sh && sudo /bin/bash aptos_dev.sh
journalctl -u aptosd -f
systemctl restart aptosd
curl 127.0.0.1:9101/metrics 2> /dev/null | grep aptos_state_sync_version
wget -q -O aptos_update.sh https://api.nodes.guru/aptos_update.sh && chmod +x aptos_update.sh && sudo /bin/bash aptos_update.sh
