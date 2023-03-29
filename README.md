# Install and use AWS-based Wireguard
Scripts automate the installation and use of Wireguard on AWS with Ubuntu Server 22.04

## How use

### Installation
```
git clone https://github.com/pprometey/wireguard_aws.git wireguard_aws
cd wireguard_aws
sudo ./initial.sh
```

The `initial.sh` script removes the previous Wireguard installation (if any) using the `remove.sh` script. It then installs and configures the Wireguard service using the `install.sh` script. And then creates a client using the `add-client.sh` script.

### Add new customer
`add-client.sh` - Script to add a new VPN client. As a result of the execution, it creates a configuration file ($CLIENT_NAME.conf) on the path ./clients/$CLIENT_NAME/, displays a QR code with the configuration.

```
sudo ./add-client.sh
#OR
sudo ./add-client.sh $CLIENT_NAME
#OR Pipe to File
./add-client.sh student02 > student02.conf
```

### Reset customers
`reset.sh` - script that removes information about clients. And stopping the VPN server Winguard
```
sudo ./reset.sh
```

### Delete Wireguard
```
sudo ./remove.sh
```
## Contributors  (alphabetically)
- [Alexey Chernyavskiy](https://github.com/alexey-chernyavskiy)
- [Max Kovgan](https://github.com/mvk)
