# Rougue tower 
## Discription 

A suspicious cell tower has been detected in the network. Analyze the captured network traffic to identify the rogue tower <br>
find the compromised device, and recover the exfiltrated flag.  

## Solution 
### hint 

<img width="502" height="214" alt="image" src="https://github.com/user-attachments/assets/8e513155-44d6-4006-8284-7102fc228afb" />


### step1
Tiến hành mở file `rouge_tower.pacap` lên và thấy dc có 3 `pack` có giao thức `UDP` 
### Pack 1
<img width="904" height="109" alt="image" src="https://github.com/user-attachments/assets/78e45fcb-ce12-4c6b-b99f-f393d6b582c7" />

### Pack 2
<img width="905" height="111" alt="image" src="https://github.com/user-attachments/assets/cc65ac30-edfe-43e4-9fdb-b6695a914960" />

### Pack 3
<img width="908" height="104" alt="image" src="https://github.com/user-attachments/assets/889c923d-7a10-44f4-85d7-ae7509d97cc6" /><br>
<br>
<br>
Thấy được ở Pack thứ 3 có thông tin về gói mạng trái phép có `PLMN=00101` và `CELLID=92130` 

### step2 
Sau khi có được `CELLID` của gói mạng trái phép là `92130` thì tiến hàng phân tích <br>
và tìm thiết bị kết nối vói gói mạng đó mạng trái phép dó <br>

Kiểm tra các Pack có giao thức ` HTTP GET` để tìm thiết bị truy cập vào gói mạng trái phép <br>

<img width="1919" height="392" alt="image" src="https://github.com/user-attachments/assets/4dc41603-4d73-4ad8-9d33-a0c16401a540" />
<img width="1913" height="123" alt="image" src="https://github.com/user-attachments/assets/dd40b36e-cd71-4e0f-9816-e7a4fb5f14d0" />




Vậy `IMSI` của thiết bị truy cập vào gói mạng là: 

```text
310410868411126
```

### step3 

Tiến hành tra cứu dữ liệu được chia nhỏ mà thiết bị đã gửi thông qua
các `pack` có giao thức `HTTP POST` để tìm flag .
















