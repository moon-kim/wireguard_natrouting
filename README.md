# wireguard_natrouting

Add the following to wg0.conf:

PostUp = /etc/wireguard/add-nat-routing.sh

PostDown = /etc/wireguard/remove-nat-routing.sh
