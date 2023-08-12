# source:
```
# devices:
## motherboard
ASUS_H110M-AM.2="W25Q128.V"    # { make: Winbond, model: W25Q128.V }
ASRock_H110M-HDS="MX25L6473E"   # { make: Macronix International, model: MX25L6473EPI }

## network
### router
NetGearRouter="MX25L6406E/MX25L6408E"

chip=$ASRock_H110M-HDS

read(){
  sudo flashrom --programmer ch341a_spi -c $chip -r original.bin
}

write(){
  sudo flashrom --programmer ch341a_spi -c $chip -w new.bin
}
```
