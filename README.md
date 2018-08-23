#### "개념 없는 운영자가 소유한 카페들은 매물로 팔리기도 합니다." 책 <창작자의 나라>(김인성) 중.....

# 여러분의 카페는 안녕하십니까?

얼마전 제가 활동하던 한 제조사의 스마트폰 관련 카페 매각사태 이후 그 충격에서 벗어나지 못하고 있는 유령회원 정해준(wjdgowns77)입니다.    
["여러분의 카페는 안녕하십니까"]     
네? 안녕하시다구요? 그렇다면 계속 안녕하리란 보장은 있으십니까?   
네이버카페는 국내 많은 사용자가 이용하고 있지만, 사용자가 많아지면 많아질수록 위험한 커뮤니티 방식입니다.    
생성과 운영이 쉬워 우후죽순 생겨난 커뮤니티 중에는 운영자가 불어난 카페의 몸집을 감당할만한 능력이 되지 않는 경우도 있습니다.  
제가 말하는 능력이란, 조그마한 금전과 사익에 흔들리지 않고 커뮤니티를 지켜내는 능력입니다.    
물론 운영능력도 필요하겠지만, 이는 논외로 합니다.    
가장 갖기 힘든 능력이 운영능력인데, 사실 가장 중요한 능력은 정상적인 개념입니다.              
[""개념 없는 운영자가 소유한 카페들은 매물로 팔리기도 합니다." 책 <창작자의 나라>(김인성) 중....."]
      
# 백업에 대한 대책     
네이버카페는 특성상 외부 크롤러의 진입이 원천 차단되어 있습니다. 구글 웹캐시, waybackmachine 아무것도 네이버 카페에 접근할수 없습니다.    
그 어떠한 외부 단체도 네이버 정책상 네이버카페에 접속할 수 없습니다.   
원본은 하나밖에 없고, 원본은 매우 불안합니다.    
개인의 일탈이 수많은 자료를 영원히 사라지게 만들 수 있습니다. 

# 스크립트(프로그램)에 대한 소개/사용방법
### 소개
NCBP(네이버카페백업프로그램)은 기초적인 파이썬 스크립트입니다.            
파이썬 스크립트를 통해 구글 크롬을 제어하여 카페 게시글을 게시글번호 기반으로 접속하여 html로 저장, 이후 이를 다시 pdf로 변환합니다.    
능력이 되시는 분들은 만들어 쓰시겠지만, 못 만드시는 분들도 좀 있으십니다. 예를 들면 일년전의 저라던가...일년전의 저라던가.....일년전의 저라던가...일년전의 저라던가......     
다른 프로그램이랑은 다르게 크롤링 중인 페이지를 직접 잘 되고 있나 확인하실 수 있고, 직접 개입하실수도 있습니다.        
네이버카페 백업 프로젝트라 하니까 네이버 카페만 될것 같죠? 사실 링크 뒤에 게시글번호 붙이는 사이트 웬만하면 다 됩니다.(물론 조금 수정하셔야 해요. 이메일 주시면 도와드립니다)       
로그인 절차가 복잡하고 캡차가 있다구요? 그럼 크롬창에서 직접 로그인 하시면 되고 직접 캡차 입력하시면 되요.     
게다가 직접 크롬을 띄워서 동작하는 거다보니 크롤링 한다고 티도 잘 안납니다.       
단, 성능(효율성)이 좋은 편은 아닙니다..... 컴퓨터 웹서핑 속도가 느리면 크롤링 자체가 오래걸립니다.            
이참에 성능 좋은걸로 한대 사셔도.........아닙니다                   
            
일단 저는 miniconda와 jupyter notebook, 창문10(win10 Build 16299.RS3)으로 기본 테스트를 했습니다.      
능력이 있으시다면 대충 소스만 가져다 쓰셔도 됩니다... 아이디어만 갖다 쓰셔도 좋고....그러니까 공개하는 거지요....ㅎㅎ     
물론, 소스 갖다 쓰시고 나서 그걸로 만든 프로그램 공유도 해주시면 더 좋구요,,,    
### 스크립트 사용을 위한 사전 설정 방법.   
1.miniconda를 받아서 설치해 줍니다.     
2.Anaconda Prompt를 여셔서 pip install jupyter, pip install selenium, pip install bs4 해 줍니다.   
2.wkhtmltopdf를 받아서 설치해 줍니다. 단, 설치 설치 경로를 변경하지 않습니다.(변경하시고 이에 맞추셔서 스크립트를 수정하셔도 되는데....귀찮은거 싫어하신다면 그냥 기본 디렉터리(설치경로)에 설치하시는걸 추천드립니다;;;;^^)   
3.크롬드라이버를 받으셔서 C드라이브에 chromedriver폴더 만드시고, 그 안에 chromedriver.exe파일을 넣어 줍니다.    
4.C드라이브의 Users 폴더 안의 사용자이름으로 된 폴더 안( C:/Users/%username% )에 cafe라는 폴더를 하나 만들어 줍니다. 크롤링 결과물이 여길로 들어가요...    
### 본격 크롤링 하는법
1.anaconda prompt를 여셔서 jupyter notebook치고 엔터 하시면 창이 뜹니다.    
2.이 스크립트를 다운받으셔서 실행하셔도 좋고, New python3 하셔서 스크립트를 한 덩어리씩 복사 붙혀넣기 하셔도 좋습니다. 어떻게든 실행만 하시면 됩니다. 단, "위에서부터 아래로" 순서대로 실행하셔야 합니다.(반대로 하시면 오류가....)  
3.오류발생시 admin@nonaver.com(주 이메일)로 연락주시면 도와드릴수도 있습니다.(저도 이걸 잘 하는게 아니기 때문에 도움을 못 드릴수도 있습니다,,) 
  
# 라이선스(사용권한)      
라이선스(사용권한)은 간단히 GNU-GPL 입니다.    
GPL에 대해 간단히 설명을 드리자면, 제 스크립트(소스)를 어떻게 쓰시든지 자유이지만, 그걸로 뭔가 다른 프로그램을 만드셨으면 그 만든 결과물을 저랑 같은 라이선스(GPL)로 배포하셔야 합니다. https://namu.wiki/w/GPL       
곤란하시다면 이메일 주세요~       

# 파일 다운받기 
[ipynb파일 받기](http://ncbp.nonaver.com/NaverCafeBackupProgram.ipynb)  
[파일보기](https://github.com/wjdgowns77/NaverCafeBackupProject/blob/master/NaverCafeBackupProgram.ipynb)     
[깃허브 페이지 보기](https://github.com/wjdgowns77/NaverCafeBackupProject/) 
  
# 링크
[이곳 링크](http://ncbp.nonaver.com)          
[제가 활동중인 카페](https://cafe.naver.com/skyplanet)        
[개인 홈페이지](http://imholic.com)       
[팬택 휴대폰 PDL파일 다운로드](http://imholic.kr)          
      
      
            
                  
                  
                  
p.s.: 제가 도메인이 좀 많지요? 안그래도 도메인 사날리다가 허리휘게 생겼습니다.....근데 조만간 더 사야해요....   
어쩌다가 회사 도메인들을 사모으는 악취미가 생겨가지고.....어휴.....ㅠㅠ        
특히 휴대폰 회사 도메인 잘못 팔렸다가는 제조사 선탑재앱이 백도어나 악성코드 배포처가 될수도 있기에 팔수도 없네요.        
조만간 도메인 등록비가 일년에 22만원씩 나올 일도 멀지 않은것 같습니다.       


admin@nonaver.com
