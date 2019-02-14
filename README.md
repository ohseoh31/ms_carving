# ms_carving

- encase에서 비할당 영역에 존재하는 MS 파일을 카빙하는 코드를 구현하려 합니다.

- 아래의 그림에서 확인 할 수 있듯이 비할당 영역의 크기가 너무 큰것을 확인 할 수 있습니다.
---  
![image](https://user-images.githubusercontent.com/15623089/52808111-77a2ce80-30d0-11e9-95bc-6b9bc25d9f0a.png)

- 비할당 영역의 데이터가 너무 많아서 임의로 D드라이브 경로에 un_used라는 명으로 하나의 파일을 생성하여 분석을 시작 하였습니다.
---  
![image](https://user-images.githubusercontent.com/15623089/52808195-a456e600-30d0-11e9-8393-dfd88b033a57.png)

![image](https://user-images.githubusercontent.com/15623089/52806282-eaf61180-30cb-11e9-80c9-a16da65638eb.png)

- 카빙을 실행하여 MS office docx/xlsx/pptx등의 파일을 카빙하여 얻을 수 있었습니다.
---  
![image](https://user-images.githubusercontent.com/15623089/52808324-ebdd7200-30d0-11e9-9e23-14a567f79d39.png)
  

- 아래의 코드를 보면 MS header (50 4B 03 04 14 00 06 00)를 확인하는 코드와 trailer(50 4B 05 06)의 크기까지 만큼 카빙하는 코드를 작성하였다.
---  
![image](https://user-images.githubusercontent.com/15623089/52808434-3b23a280-30d1-11e9-9c56-93372e876da1.png)
  
- 다음으로 docx/xlsx/pptx 아래의 시그니처로 파일을 구분하는 코드로 카빙을 진행 하였습니다. 
```  
  70 70 74 2F 73 6C 69 64 65 73 2F 5F 72 65 6C 73 은 pptx로
  78 6C 2F 5F 72 65 6C 73 은 xlsx파이로
  77 6F 72 64 2F 5F 72 65 6C 73 은 word 파일
```  


- 
