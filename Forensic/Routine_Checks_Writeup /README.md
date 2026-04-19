# Routine_checks

## Description

Routine system checks were performed on the city’s communication network after reports of instability.
Operators sent brief messages between nodes to confirm everything was running smoothly.
Most of the exchanges are ordinary status updates, but one message stands out as… different.
Author : Gopi

Flag forma: apoorvctf{.........}

## Solution 

### step1
sau khi tải file `challenge.pcap.xz1 về thì giải nén nó ra mà mở bằng công cụ `wireshark`

### step2 
sau khi mở file lên thì thấy được rằng ở dòng `no.14` có độ dài dữ liệu bất thường 
chúng ra thao tác xem dữ liệu bênh trong nó theo thứ tự ` chuột phải ` --> ` show ` --> `show in tcp stream `

### step3 
ta thấy được dữ liệu ở dạng ` ASSCI ` bắt đầu bằng chữ " JFIF " thì biết đây là dữ liệu của 1 file ảnh ` file.jpg ` or `file.speg` 
ra đổi dạng dữ liệu thành " RAW " , đây là dạng dữ liệu được mã hóa ` HEX ` 
dùng công cụ `" CYBERCHEF " ` để DECODE  và add thêm chức năng RENDER IMAGE để render dữ liệu thành file ảnh 
<img width="99" height="99" alt="flag" src="https://github.com/user-attachments/assets/1afe4844-b238-4cdb-b7e8-8cf9a40d7740" />


### step 4
sau khi có được file ảnh là 1 mã QR CODE thì đây là 1 flag troll 
tiến hành phân tích sâu cấu trúc của ảnh để tìm flag bằng công cụ ` " APERI SLOVE " ` thì ra thấy được rằng flag được giấu ở dạng ` Steghide ` thì ở mục Steghide 
có giấu 1 file` realflag.txt ` ta tải file về và mở bằng NOTEPAD 
### FLAG:  apoorvctf{b1ts_wh1sp3r_1n_th3_l0w3st_b1t}
