# I2C Control

### I2C 란?

`Inter-Integrated Circuit`
 Serial Communication 

> PIN
>
> * SDA : Serial Data Line
> * SCL : Serial Clock Line

> 특징
>
> * i2c device는 보통 7bit address를 사용하며 실제 사용시에는 7bit 주소값에  read/write flag를 붙여서 사용한다.
>   -> read flag=1, write flag=0
> * baud rate를 사용하는 비동기 통신 방식



### 일반적인 I2C Control

i2c device 이용

i2c device로 사용할 경우 `i2c-x`형태의 디바이스를 사용할 수 있다. -> 디바이스 드라이버 사용하여 접근 가능
i2c 디바이스 드라이버를 사용할 경우 간단한 테스트는 `i2c-tools`를 이용가능하다.

또는 device file을 열어 사용 가능하다.

> I2C Device Driver 사용 방법
>
> 1. /dev/i2c-x 디바이스 드라이버 파일 오픈
> 2. ioctl을 사용하여 slave address 설정
> 3. read(), write() 함수를 사용하여 i2c device의 레지스터의 값을 읽거나 쓸 수 있음.



### MMAP을 이용한 직접 i2c 컨트롤

작성..?!