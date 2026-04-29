# Rougue tower 
## Discription 

A suspicious cell tower has been detected in the network. Analyze the captured network traffic to identify the rogue tower <br>
find the compromised device, and recover the exfiltrated flag.  

## Solution 
### hint 

<img width="313" height="232" alt="image" src="https://github.com/user-attachments/assets/5160afee-b915-4e10-b2ef-a7b813650abb" />
<img width="310" height="246" alt="image" src="https://github.com/user-attachments/assets/85cc766d-4eea-4315-b8f9-573033a7a620" />


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
Sau khi có được `CELLID` của gói mạng trái phép là `92130` thì tiến hàng phân tích và tìm thiết bị kết nối.  <br>
Kiểm tra các Pack có giao thức ` HTTP GET` 















