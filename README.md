## 로또 6/45 추첨결과 정보
1회부터 최근회까지 추첨결과를 json으로 제공합니다.  
(본 정보에는 오류가 있을 수 있으며, 동행복권 사이트에서 정확한 당첨번호를 확인하실 수 있습니다.)

### 조회방법

회차별 조회
```
https://smok95.github.io/lotto/results/{회차번호}.json
```
최근회차 조회
```
https://smok95.github.io/lotto/results/latest.json
```
전체회차 조회
```
https://smok95.github.io/lotto/results/all.json
```

### 형식
```code
{
 "draw_no": 929,
 "numbers": [7, 9, 12, 15, 19, 23],
 "bonus_no": 4,
 "date": "2020-09-19T00:00:00Z",
 "divisions": [
  {"prize": 1308035157, "winners": 16},
  {"prize": 38330701, "winners": 91},
  {"prize": 1151947, "winners": 3028},
  {"prize": 50000, "winners": 140880},
  {"prize": 5000, "winners": 2244712}
 ],
 "total_sales_amount": 92344620000,
 "winners_combination": {
  "auto": 9, "semi_auto": 1, "manual": 6
 }
}
```
```
draw_no: 회차
numbers: 당첨번호
bonus_no: 보너스 번호
divisions: 1~5등 당첨인원 및 1인당 당첨금액
[
    prize:  1인당 당첨금액
    winners: 당첨인원
]
total_sales_amount: 총 판매액
winners_combination: 1등 번호선택유형
{
    auto: 자동 인원수
    semi_auto: 반자동 인원수
    manual: 수동 인원수
}
```



---



## 로또 6/45 1등 배출점 정보
262회부터 최근회까지 추첨결과를 json으로 제공합니다.  
(본 정보에는 오류가 있을 수 있으며, 동행복권 사이트에서 정확한 정보를 확인하실 수 있습니다.)

### 조회방법

회차별 조회
```
https://smok95.github.io/lotto/winning-stores/{회차번호}.json
```

### 형식
```code
[
 {
  "name": "태극로또전문점",
  "address": "경기 이천시 애련정로 124-2",
  "combination": "자동",
  "lat": 37.28148,
  "lng": 127.4503
 },
 {
  "name": "대박로또복권",
  "address": "강원 원주시 관설동  1771-6패밀리마트관설에버빌점",
  "combination": "자동",
  "lat": 37.315277,
  "lng": 127.96166
 }
]
```
```
name: 점포명
address: 소재지
combination: 자동/수동 구분 ("자동","수동","반자동" 중 하나)
lat: 위도
lng: 경도
```