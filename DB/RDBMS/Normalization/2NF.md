# 제 2 정규형

## 제 2 정규형이란...
릴레이션이 제 1 정규형에 속하고, 기본키가 아닌 모든 속성이 기본키에 완전 함수 종속 되는 것을 말함 

### 제 1 정규형에서 생길 수 있는 문제점
|<u>고객아이디</u>|<u>이벤트 번호</u>|당첨여부|등급|할인율|
|---|---|---|---|---|
|apple|E001|Y|gold|10%|
|apple|E005|N|gold|10%|
|apple|E010|Y|gold|10%|
|banana|E002|N|vip|10%|
|banana|E005|Y|vip|10%|
|carrol|E002|N|vip|10%|
|carrol|E005|Y|vip|10%|
|orange|E004|N|silver|10%|

