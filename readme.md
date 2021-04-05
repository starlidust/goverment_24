## 계기
정부24에서 건축물대장 등을 떼는데 너무 많은 품이 들어간단 사실이 안타까움   
그래서 자동화 가능한지 실험했고 가능하다고 판단했다.

## 사전설치
anaconda  
chromedriver  
Beautifulsoup, seleium   

* module  
!pip install Beatifulfsoup4  
!pip install seleium  

* chromedriver  
현재사용하고 있는 크롬과 동일한 버전의 크롬드라이버를 다운받고 코드가 있는 위치에 저장   
[chromdriver 다운](https://chromedriver.chromium.org/downloads)  

## 방법
셀레니움으로 마우스,입력을 조작하여 반복해서 해야하는 행동을 컴퓨터가 대신하게함  
단, 너무 빠른속도로 움직이게 되면 봇 판정을 받을 수도 있고, 서버에 과부화가 걸릴것으로 예상되어   
중간중간 쉬는시간을 넣어줌  

최종적으로 엑셀파일을 만드는 것이 목표이나, 열람 외 발급의 경우 크롤링이 불가 (이미지파일)  
따라서 엑셀로 만드는 작업을 열람에만 해당

### code1
아파트 내 모든 동,호의 표제부로 소유권을 확인하는 코드   
4단계로 구성되어 있다.  
1단계는 해당 아파트 내에 있는 모든 동의 개수를 파악한다  
2단계는 해당 아파트 특정 동 내에 있는 호수를 파악하고 첫번째를 열람신청한다.  
3단계는 해당 아파트 특정 동 내에 있는 모든 호수를 열람신청한다.  
4단계는 열람신청한 결과물을 엑셀로 변환한다.  