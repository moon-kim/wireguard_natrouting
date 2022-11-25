# wireguard_natrouting

Add the following to wg0.conf:

PostUp = /etc/wireguard/helper/add-nat-routing.sh

PostDown = /etc/wireguard/helper/remove-nat-routing.sh
