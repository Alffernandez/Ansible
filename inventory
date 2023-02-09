#!/usr/bin/env bash
# id: scripts/inventory-script.sh

cat << EOF
{"all": {"hosts": ["ansible02"], "children":
["Nodos-tower"]}, "Nodos-tower": {"hosts": ["ansible01"]}, "_meta":
{"hostvars": {"ansible01": {"ansible_host": "172.29.59.10",
"remote_tower_enabled": "true", "remote_host_enabled": "true",
"remote_host_id": 2}, "ansible02": {"ansible_host": "172.29.59.12",
"remote_tower_enabled": "true", "remote_host_enabled": "true",
"remote_host_id": 3}}}}
EOF
