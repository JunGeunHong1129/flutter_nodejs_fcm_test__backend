# flutter_nodejs_fcm_test__backend

## FCM 테스트 백엔드 입니다.

## 사용법
- 푸시알람을 보내는 방법은 다음과 같습니다.             
post메소드를 사용하며 body에 내용을 담아 주셔야 합니다.  
총 **title, body, url, target, msgType, compCd, userId, compNm** 8가지입니다.    

- title : 푸시알람의 제목  
- body : 푸시알람의 내용  
- url : 이동시킬 페이지의 url  
- target : 목표 기기     
    - 목표기기 : deviceToken(devToken)    
    - 전체 : ALL  
- msgType : 메시지 타입    
    - '0'  그룹핑을 위해 사용금지 
    - '1'  게시판 
    - '2'  서류함    
**반드시 int로 구분해서 보내야 합니다.**
- compCd : 목표 업체 코드    
- userId : 목표 업체의 아이디    
- compNm : 목표 업체명    
**target을 넣어서 보내지 않으면 400 에러를 보냅니다. 반드시 넣으시기 바랍니다.**      
          

## 주의사항
- url syntax에 맞게 %0a를 넣으면 스낵바 내부에서 줄바꿈기능이 지원됩니다.               
그러나 현재 푸시알람은 줄바꿈기능을 지원하지 않습니다. (카톡알람과 비슷합니다)              
푸시알람에 한눈에 보이는 바디를 구성하고 싶다면 20자 내에서 처리해주세요.               
**target을 넣어서 보내지 않으면 400 에러를 보냅니다.!!!**              