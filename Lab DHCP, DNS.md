# Cài đặt isc-dhcp-server

Cài đặt isc-dhcp-server

    sudo apt install isc-dhcp-server

Backup file `dhcpd.conf`
![image](https://user-images.githubusercontent.com/54473576/224598835-fd7b219a-aafa-416a-8e1d-1e0af8adc46d.png)

Dùng `sudo mv dhcpd.conf dhcp.conf.bakup` để backup file

![image](https://user-images.githubusercontent.com/54473576/224599178-2c6b8ce6-87f9-4cd5-a31b-f41b0e561aeb.png)

Dùng `sudo /etc/dhcp/dhcp.conf` để sửa file config

Dùng `ifconfig (yourinterface)  (your static IP)/(mask number)` để cài IP cho DHCP server

```

    Network : 172.16.10.0
    NetMask : 255.255.255.0
    Gateway : 172.16.10.1
    DNS1 : 8.8.8.8
    DNS2 : 8.8.4.4
    IP Server : 172.16.10.10
# To specify the default and maximum lease time 
default-lease-time 600;

max-lease-time 7200;

ddns-update-style none;

authoritative;

subnet 172.16.10.0 netmask 255.255.255.0
{

        range 172.16.10.100 172.16.10.200;
        option routers 172.16.10.10;
        option subnet-mask 255.255.255.0;
        option domain-name-servers 8.8.8.8, 8.8.4.4;
}
```

Dùng `sudo systemctl restart isc-dhcp-server` để khởi động dịch vụ `isc-dhcp-server`

Dùng `sudo systemctl enable isc-dhcp-server` để bật dịch vụ `isc-dhcp-server`

![image](https://user-images.githubusercontent.com/54473576/224599871-f7cf74f1-1dec-4c40-9a1a-9aea3c50b02e.png)

Dùng `sudo systemctl status isc-dhcp-server` đẻ kiểm tra dịch vụ

![image](https://user-images.githubusercontent.com/54473576/224600045-e4a8c294-7452-49cc-b2d3-2a1a3f88b841.png)

Sang máy khác kiểm tra :))

![image](https://user-images.githubusercontent.com/54473576/224600204-296384db-91d6-4a40-94bf-a2a9d054a0a2.png)

