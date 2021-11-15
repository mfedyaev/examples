# Filter Instance Names and IPs from terraform with jq
cat terraform.tfstate | jq '.resources[].instances[].attributes | {name: .tags.Name, public_ip}'
