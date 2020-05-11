### "개념 없는 운영자가 소유한 카페들은 매물로 팔리기도 합니다." 책 <창작자의 나라>(김인성) 중.....      
###### 물론 꼭 이게 아니더라도 종종 카페 백업할 일은 생기긴 합니다. 그러나, 저에게 메일을 주시는 분의 상당수는 위의 사유로 인해 급히 백업을 진행하시는 분들이십니다.     
     
# 여러분의 카페는 안녕하십니까?
     
안녕하세요? 얼마전 제가 활동하던 스마트폰 관련 카페인 SDA 카페의 매각 사태 이후 그 충격에서 벗어나지 못하고 있는 유령회원 정해준(wjdgowns77)입니다.    
#### "여러분의 카페는 안녕하십니까"      
네이버카페는 국내의 많은 사용자가 이용하고 있지만, 신뢰도는 매우 낮은 커뮤니티 방식 중 하나입니다.    
생성과 운영이 쉬워 우후죽순 생겨난 커뮤니티 중에는 운영자가 불어난 카페의 몸집을 감당할만한 자격이 되지 않는 경우가 있고, 네이버는 이러한 상황이 발생해도 이를 방치할 뿐 아무런 조치를 하지 않습니다.      
그 결과로 인터넷 독재와 카페 매각이라는 카페매니저의 부적절한 행동에 방대한 데이터가 유실되는 경우도 있습니다.       
네이버카페는 특성상 외부 크롤러의 진입이 원천 차단되어 있어 구글 웹캐시, waybackmachine 등이 네이버 카페에 접근할수 없어 복사본이 하나도 없지만, 원본이 매우 불안합니다.    
단 한 사람의 잘못된 행동이 수많은 자료를 영원히 사라지게 만들 수 있습니다.      
     
     
# 스크립트(프로그램)에 대한 소개/사용방법
### 소개
NCBP(네이버 카페 백업 프로그램)은 파이썬을 기반으로 만들어져 있습니다.            
파이썬 스크립트를 통해 구글 크롬을 제어하여 카페 게시글을 게시글 번호를 기반으로 접속하여 html로 저장, 이후 이를 다시 pdf로 변환합니다.    
다른 프로그램이랑은 다르게 크롤링 중인 페이지를 직접 잘 되고 있나 확인하실 수 있고, 직접 개입하실수도 있습니다.        
단, 성능(효율성)이 좋은 편은 아닙니다. 컴퓨터 웹 서핑 속도가 느리면 크롤링 자체가 오래걸립니다.            
현재 배포되는 NCBP의 배포판은 파이썬의 기본 프로그램인 idle에서 돌아가고, 대부분의 외부 프로그램들을 내장해서 크롬을 빼고는 따로 설치할 프로그램은 없습니다. (크롤링에 사용되는 파이썬(miniconda),wkhtmltppdf등의 프로그램들은 NCBP를 설치하면서 자동으로 함께 설치됩니다.)     
    
### 사용방법
[이곳](https://github.com/wjdgowns77/NaverCafeBackupProject/tree/master/ver0.32)  을 참고하셔서 설치를 위한 zip파일을 받으시고, 압축을 풀어주세요.   
압축을 푸신 후, 해당 파일 내에 있는 install.bat파일을 더블클릭하시면 자동으로 설치가 진행됩니다.     
설치파일 내에는 파이썬과 wkhtmltopdf같은 필수 설치파일이 포함되어 있어 별도로 받으셔서 설치하셔야 할 부분은 아마 없으실 겁니다.   
설치가 완료된 후, 바탕화면에 있는 NaverCafeBackupProgram 바로가기를 실행하시고 창에서 지시하는대로 값을 입력하신 후 크롤링을 진행하시면 됩니다.   
중간에 뜨는 검은 CMD창은 WKHTMLTOPDF프로그램으로, 창 닫으시면 안됩니다! 저장한 HTML파일을 PDF로 다시 저장할때 사용되는 파일인데, 보통 2-10개정도는 같이 떠 있어도 괜찮습니다.(참고로 창이 생기기만 하고 겁나게 쌓여가지고 너무 안 없어진다 싶으시면 크롤링 딜레이를 너무 짧게 잡으신 겁니다. 2 ~ 3초 정도 더 풀어주세요~ )      
크롤링된 파일은 C:\Users\(사용자이름)\NCBP\CAFE 에 저장됩니다.     
     
그리고, 혹시, 크롬 브라우저를 설치하지 않으셨다면, 별도로 설치하셔야 합니다.(Chrome설치파일은 내장되어 있지 않습니다.)    
     
     
# 사용중 문제 발생시.       
사용중 문제 발생시 Admin@NoNaver.com 이메일로 해당 스크린샷을 찍어서 보내주시면 최대한 도움을 드리겠습니다.    
또, 사용에 있어 불편한 점이 아주 많으실 것을 알고 있고, 개발에 대해 조언하시고 싶으신 것도 아마 아주 많으실 겁니다.  
메일로 보내주시면 최대한 개선해 보겠습니다.(욕을 보내셔도 됩니다만, 꼭 이유를 함께 보내주세요.)     
카페 규모와 상황에 따라 제가 대신 해드릴수도 있습니다.(물론, 100% 무료입니다.)    
     
        
# 언인스톨    
uninstall.bat파일을 실행하시면 자동으로 삭제가 진행됩니다.
단, miniconda와 wkhtmltopdf는 프로그램 추가/제거에서 별도 삭제를 진행하셔야 합니다.    
     
     
# 추후 개발계획      
- 현재 출력파일 형식은 *.html, *.pdf형식입니다.   
- 이미 생성된 html파일을 pdf로 변환하는 과정에서 절대경로가 지정되지 않고 상대경로가 지정되어있는 경우에 한해 사진 깨짐등의 문제가 발생하고, 네이버카페의 경우 절대경로를 지정하고 있어 이 문제는 없습니다만, 해당 프로그램을 사용하여 네이버카페만 크롤링이 가능한게 아니므로 최대한 빠른 시일 내에 *.jpeg형식으로 스크린샷을 찍어 저장하는 방식도 추가할 생각입니다. 
- 첨부파일 저장 안되는 부분에 대해 많은 분들께서 조언주셨습니다. 나중에 첨부파일도 같이 저장할 수 있도록 개선해 보겠습니다만, 언재가 될지 잘 모르겠습니다(게을러서 죄송합니다...ㅠㅠ)
     
     
# 라이선스(사용권한)      
라이선스(사용권한)은 간단히 GNU-GPL v3 입니다.    
GPL에 대해 간단히 설명을 드리자면, 제 스크립트(소스)를 어떻게 쓰시든지 자유이지만, 그걸로 뭔가 다른 프로그램을 만드셨으면 그 만든 결과물을 저랑 같은 라이선스(GPL)로 배포하셔야 합니다. https://namu.wiki/w/GPL       
곤란하시다면 이메일 주세요~ 별도 요청시 전염성 제거된 GPL라이선스로도 배포 가능합니다~~   
     
         
# 파일 다운받기 
[설치용 zip파일 받기](https://imholic.com:8081/fbsharing/1zaaLJiJ)  
[ver0.33 github페이지](https://github.com/wjdgowns77/NaverCafeBackupProject/tree/master/ver0.33)    
[설치파일 스크립트 보기](https://github.com/wjdgowns77/NaverCafeBackupProject/blob/master/ver0.33/install.bat)     
[크롤링 스크립트 보기](https://github.com/wjdgowns77/NaverCafeBackupProject/blob/master/ver0.33/programdata/NCBP.py)
 
# 링크
[이곳 링크](http://ncbp.nonaver.com)          
[개인 홈페이지](http://imholic.com)             
      
      
            
                  
                  
                  


admin@nonaver.com
