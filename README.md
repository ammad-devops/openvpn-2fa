OpenVPN is a VPN package, in order to make a connection to your resources on a private network. To add another layer of security, we’re adding a 2FA mechanism for each user. They will login as usual, but will need to use a time-based token (provided by the Authy app on their phone) to login to company’s networks.

Installation:

First need to disable SELinux(if you’re using SELinux)

vim /etc/selinux/config
SELINUX=disabled

and add IPv4 forwarding

vim /etc/sysctl.conf
net.ipv4.ip_forward=1

Reboot the server.

Create a new directory /opt/openvpn

# openvpn-2fa
# openvpn-2fa
