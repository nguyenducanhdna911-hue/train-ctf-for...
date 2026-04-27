# Recovered Signal File  <br>
## Description   <br>

This signal was recovered from a Cold War-era satellite. The encryption doesn't appear very advanced, but it was enough to avoid detection at the time.  <br>
With the right approach, the message should be recoverable.  <br>
Flag format for this challenge is flag{}.  <br>

## Solution   <br>

mở file `signal.log` lên bằng notepad lên thì có có được nội dung như sau :<br>   
```text
Recovered Signal File  
Satellite: KOSMOS-1962  
Year: 1962 
Location: Low Earth Orbit  
Status: Signal degraded  
Encoded Transmission:   
aW9kant2ZHdob29sd2hfdmxqcWRvX2doZnJnaGd9
```

Nội dung truyền tải mã hóa là :  <br>
`aW9kant2ZHdob29sd2hfdmxqcWRvX2doZnJnaGd9` đây là đoạn mã hóa 2 lớp là `base64` và `ROT13`   <br>
với nội dung chuyền tải sau khi decode bằng `base64` thì được  <br>
`iodj{vdwhoolwh_vljqdo_ghfrghg}`   <br>

Nếu lùi 3 ký tự lại thì sẽ lần luợt thu được  :  <br>
`i --> f`   <br>
`o --> l`   <br>
`d --> a`  <br>
`j --> g`   <br>
vì vậy tiếp tục tiến hành decode bằng ` ROT13 ` với giá trị Amount là `23` , để lùi lại 3 ký tự .  <br>

### FLAG : flag{satellite_signal_decoded}








