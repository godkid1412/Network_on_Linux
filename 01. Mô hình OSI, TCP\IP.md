# Mô hình OSI

| Mô hình OSI  |                                                      |
| :----------: | :--------------------------------------------------- |
| Application  | File, print, message, database, application services |
| Presentation | Data encryption, compression, translation services   |
|   Session    | Dialog control                                       |
|  Transport   | End-to-end connection                                |
|   Network    | Routing                                              |
|  Data Link   | Framing                                              |
|   Physical   | Physical topology                                    |

# Mô hình TCP/ IP

<img width="410" alt="image" src="https://user-images.githubusercontent.com/54473576/223312572-d6d75827-8123-41f1-9e0e-23b2137ecf67.png">

- Telnet: Cho phép user (Telnet Client) truy cập tài nguyên của máy khác (Telnet Server)
- File Transfer Protocol (FTP): giao thức để truyền file giữa 2 máy.
- Trivial File Transfer Protocol (TFTP): Là phiên bản đơn giản hoá của FTP.
- Network File System (NFS): là hệ thống chia sẻ dữ liệu trên các hệ thống vật lý
- Simple Mail Transfer Protocol (SMTP):
- Simple Network Management Protocol (SNMP):
- Domain Name Server (DNS):
- Dynamic Host Configuration Protocol (DHCP)

# TCP vs UDP

| TCP                                              | UDP                                         |
| ------------------------------------------------ | ------------------------------------------- |
| Đảm bảo rằng dữ liệu đến đúng như khi được gửi.  | Không đảm bảo dữ liệu đến                   |
| Kiểm tra lỗi các luồng dữ liệu                   | Không cung cấp tính năng kiểm lỗi           |
| Header 20 byte cho phép 40 byte dữ liệu tùy chọn | Header 8 byte chỉ cho phép dữ liệu bắt buộc |
| Chậm hơn UDP                                     | Nhanh hơn TCP                               |
| Tốt nhất cho các ứng dụng yêu cầu độ tin cậy     | Tốt nhất cho các ứng dụng yêu cầu tốc độ    |

# IPv4

Được tạo từ 4 octet. Mỗi octet có 8 bit

| 128 | 64  | 32  | 16  |  8  |  4  |  2  |  1  |  Biary value  |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-----------: |
|  1  |  0  |  0  |  0  |  1  |  1  |  0  |  1  | Byte in biary |

## Network Address Range: Class A

00000000 = 01

01111111 = 127

## Network Address Range: Class B

01000000 = 128

11000000 = 191

## Network Address Range: Class C

11000000 = 192

11011111 = 223

## Network Address Renge: Class D

11100000 = 224

11101111 = 239

## Network Address Range: Class E

11110000 = 240

11111111 = 255

## subnet, broadcast address, valid host range

| 172.16.10.5     | 10101100.00010000.00001010.00000101 |
| --------------- | ----------------------------------- |
| 255.255.255.128 | 11111111.11111111.11111111.10000000 |

# IPv6
