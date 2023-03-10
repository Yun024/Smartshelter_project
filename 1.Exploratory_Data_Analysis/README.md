# 탐색적 데이터 분석

```
- 본격적인 분석에 들어가기에 앞서 데이터의 분포 및 값을 검토
- 데이터가 표현하는 현상 혹은 데이터에 대한 잠재적인 문제를 발견할 수 있음
- 이를 바탕으로 기존의 가설을 수정하거나 새로운 가설을 세울 수 있음 
```

## Excel
- 승하차객이 많은 대전 버스 정류장 TOP 10 그래프 

<img src="https://user-images.githubusercontent.com/52143231/220438444-c331c898-f7c9-40fb-8fdd-8aeb6aab937f.png"  width="500" height="300"/>

``` 
주로 지역과 지역을 연결하는 시외버스와 기차가 정차하는 지역에 이용객이 
많고 대전의 랜드마크라고 할 수 있는 은하수네거리, 으능정이거리, 유성온천
쪽에 유동인구가 많다는 사실을 확인함
```

- 대전의 자치구 별 특정인구 그래프

<img src="https://user-images.githubusercontent.com/52143231/220440520-8b443045-72e3-4c87-b55d-bbc8a3737c31.png"  width="600" height="300"/>

```
두 그래프의 차이를 통해 구별 인구의 절대적인 수치가 아닌 구별 인구의 
비율 데이터를 고려하는 것이 스마트 쉘터 입지선정에 있어 좀 더 좋은 
결과를 산출할 수 있을 것 같다고 생각함
```

- 대전의 자치구 별 400m 내 해당 시설 그래프 

<img src="https://user-images.githubusercontent.com/52143231/220440666-4ad5e115-027b-4827-ba3a-64d0a0630ed7.png"  width="600" height="300"/>

```
ㅁ 동구: 학교 수가 적은 편이지만 복지시설이 많이 위치함. 
   -65세 이상 인구가 많이 거주하는 지역으로 예상됨
ㅁ 서구: 학교 수와 복지시설 수 모두 많이 존재함, 지하철역도 다수 존재
   -19세 이하, 65세 이상 인구가 많이 거주하며 교통량이 많은 지역이라고 예상됨
ㅁ 유성구·중구: 타 자치구에 비해 뚜렷한 특징을 가지고 있지 않음
ㅁ 대덕구 : 미세먼지 발생 시설이 가장 많이 존재, 지하철역이 거의 없음
```
` 종합해보면 공공성과 이용성을 고려한 스마트 쉘터 입지 후보에 동구와 서구의 정류장이 주로 선택될 것이라고 예상됨 `



## R  
- 워드클라우드 
<img src="https://user-images.githubusercontent.com/52143231/220441326-14647055-969d-462a-82ec-b9b1e429e5bb.png"  width="500" height="400"/>

```
대전 버스의 문제점을 파악하고자 한밭대학교에서 운영하는 대전지역문제 공유 플랫폼인 
‘지역사회문제은행’에서 '대전'과 '버스'를 키워드로 민원 분석을 시행한 결과 ‘정류장’에 
관한 문제점이 가장 두드러진 것으로 확인되었음
```

- 상관계수 히트맵 

<img src="https://user-images.githubusercontent.com/52143231/220441001-dc9c16da-e27f-4781-b40f-94779a5dd88b.png"  width="600" height="400"/>

```
ㅁ ‘총인구수’ ‘19세이하’, ‘65세이상’의 인구특성 변수끼리 높은 상관성을 보임 
ㅁ ‘초승수합’, ‘환승수합’, ‘총승차객합계’의 버스이용 변수끼리 높은 상관성을 보임
```
`PCA를 통해 높은 상관도를 가진 속성들의 변동성을 소수의 PCA만으로 자연스럽게 수용할 필요가 있음 `

