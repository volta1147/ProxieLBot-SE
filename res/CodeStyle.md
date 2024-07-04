# 코드 스타일

## 목적
1. 코드간 충돌이 없고 프로그램 내 여러 코드에서 사용될 수 있도록 통일안을 마련하기 위함이다. 

## 구조
2. 바탕이 되는 코드는 가장 바깥에, 그 외 기능 실행 시 필요한 함수들은 lib 폴더 안에, 추가 기능은 Cogs 폴더 안에 위치한다.\
  프로그램에 있어서 필요한 파일들은 res폴더 안에 위치하며, 보안 상 숨겨둘 파일은 res\\security 폴더에, 그 외의 설정값을 저장한 파일은 res 폴더에 텍스트 파일로, 명세는 res 폴더에 마크다운 파일로 저장한다. \
  security 폴더에 있어야 할 항목은 security 폴더 속 securityfiles.txt에 따른다. 
3. 메인 코드는 main.py, 런처와의 호환성을 맞추는 라이브러리는 launchio.py로, 실행 시 필요한 정보를 불러오는 라이브러리는 lib 폴더 속 botsetup.py로 한다. 
4. 메모 등 커뮤니티 활동을 통해 생성되는 파일들은 community 폴더 속에 저장한다. 
5. 새로운 명령어를 추가할 때 Cogs를 사용한다. 

## 표현 방식

### 프로그래밍 구조 및 명령어

6. 모든 플랫폼과 최신 파이썬 버전에서 최대한 호환이 가능하도록 한다. 
7. Client 기반 함수들은 사용을 자제한다. 현재 프로그램의 구조인 commands.Bot을 따른다. 
8. 상호작용이 필요한 명령어는 슬래시 명령어를 사용하며, 그렇지 않은 경우는 메시지형 명령어도 허용한다.\
  메시지형 명령어는 장기적으로 제거해나가는 것을 원칙으로 한다. 

### 파일 입출력
9. 모든 파일 입출력은 launchio.py 기반으로 한다. 이는 런처와의 호환성을 유지하기 위함이다. 

### 작명
10. 기본적으로, [PEP8(파이썬 코딩 스타일에 대한 가이드)](<https://peps.python.org/pep-0008/>)를 따른다. 
11. 이름은 그 의미가 잘 드러나도록 한다. 
12. 사용처가 비슷한 함수/변수의 경우 글자 수를 맞춘다. 
13. Cogs는 첫 문자를 대문자로 하되(예시 : Memo.py), 대문자로 자주 쓰이는 단어의 경우(TTS -> TTS.py) 그대로 사용한다. 
14. 명령어 이름은 함수의 작명규칙을 따른다. 

### 명령어
15. 사용처가 비슷한 함수, 변수끼리 같은 클래스로 만들고, 다른 클래스의 것과 사용 방법이 비슷한 함수, 변수끼리는 이름을 같게 한다. 

### 스타일
16. f"{변수명}" 형식을 표준으로 한다. 
17. 상태를 나타내거나 Literal을 사용하여 특정 값을 인수로 받을 때, 또는 그런 값을 리턴할 때는 작은따옴표를 쓰고, 나머지 경우에는 큰따옴표를 쓴다. 
18. 키워드 인수나 초기값을 설정하는 부분에서는 등호 양쪽에 띄어쓰기를 하지 않는다. 
19. 타입 힌트, 타입 어노테이션은 적는 것을 기본으로 한다. 

## 선언 시 주의사항
20. prefix와 memoprefix는 다른 값을 가지는 것을 원칙으로 한다. 

## 특정 파일에 관한 규정

### 프로그램의 정체성에 관한 문서
21. 기존 문서를 삭제하고 현재 버전까지 다시 작성한다. 

### 메모 예시
22. 남아있던 메모 예시는 삭제한다. 

## 버전 작명 방식
23. (메이저 버전).(마이너 버전).(날짜코드) 형식으로 적는다. 
  불가피한 상황이 아니라면 날짜코드는 YYMN으로 한다. 단, N은 그 달에 나온 정식 버전 개수이다. (예시 : )
  10월, 11월, 12월은 각각 A, B, C로 표기한다. 
24. 현재까지 베타버전으로 계획된 버전을 정식 버전으로 승격한다. 

## 기타
25. 메모 서비스 코드 등에 쓰이는 file.py의 입출력 함수는 현재 버전에서 community\\"원본 폴더" 형태로 수정한다.\
  다음 버전까지 launchio.py 기반으로 수정한다. 
26. 기존의 메시지형 명령어 체계는 삭제하지 않고 유지한다. 
27. PEP8과 충돌하는 기존 변수들의 이름은 현재 버전까지 수정한다. 
28. 이 외에 현재 규칙과 충돌하는 개발 스타일은 다음 버전까지 수정하는 것을 원칙으로 한다. 