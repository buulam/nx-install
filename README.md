# node_exporter install script

This is a simple shell script to get node_exporter installed onto a linux host.

Pull it into a file

`
sudo wget https://raw.githubusercontent.com/buulam/nx-install/refs/heads/main/nx-install.sh -O nx-install.sh
`

Run with priveledges.

Edit /etc/prometheus/prometheus.yml

Add under static_configs:

`
      - targets: ["ip that you want to add:9100"]
        labels:
          instance: '<I've been putting hostname here>'
`
