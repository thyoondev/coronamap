# 코로나맵 프로젝트
### Development environment
- VSCode
- Node.js
- Nodemon
- Express
- [네이버 지도 API](https://navermaps.github.io/maps.js.ncp/docs/tutorial-2-Getting-Started.html)
- [카카오 지도 API](https://apis.map.kakao.com/)
- [공공데이터포털API 보건복지부_코로나19 감염_현황](https://www.data.go.kr/data/15043376/openapi.do) 
- [공공데이터포털API 보건복지부_코로나19 시·도발생_현황](https://www.data.go.kr/data/15043378/openapi.do) 


### Features
- 코로나 방문 장소 추적
- 현재 코로나 감염 현황 확인

### Screenshot
| ![https://ikeaweb.s3.ap-northeast-2.amazonaws.com/gitimg/coronamap/1.png](https://ikeaweb.s3.ap-northeast-2.amazonaws.com/gitimg/coronamap/1.png) | ![https://ikeaweb.s3.ap-northeast-2.amazonaws.com/gitimg/coronamap/2.png](https://ikeaweb.s3.ap-northeast-2.amazonaws.com/gitimg/coronamap/2.png) | 
|:---:|:---:|
| 메뉴 축소 화면 | 메뉴 확장 화면 |


### Todo
- 네이버 지도 API사용해서 맵 보여주기
- 모바일에서 보기 편하게 메뉴 축소 확장 기능
- 코로나 방문위치에 마커 생성
- 날짜별 코로나 방문 위치 색상 변경
- 공공데이터API 활용해서 자동으로 데이터 업데이트 기능
- 위치 검색기능(카카오API 사용)
- 현재 위치 확인 기능


### TIP
코로나 정보 제공 사이트들을 보고 만들어보고 싶다고 생각하던와중, 마침 코로나맵 사이트를 서비스하고 있는 개발자님의 글을 본 것이 계기가 되어서 만들어보았다.

모바일에서 보기 편하게 기본적으로 메뉴를 전부 가려놨고, 작게 만들었다. 네이버 지도 API를 사용하였는데 네이버 자체적으로 API에 대한 문서화를 잘해놔서 기능 추가에 큰 어려움은 없었다.

코로나가 발생한 곳의 데이터를 넣으면 그 위치에 마커를 표시해주고, 날짜를 비교해 날짜별로 마커의 색상을 다르게 해주어 한눈에 알아보기 편하게 하였다. 추가로 보건복지부에서 공개한 API를 활용해 당일 전국 코로나 현황과 내가 살고 있는 지역의 코로나 현황도 볼 수 있게 구현해놓았다. API는 XML이나 JSON이나 사실 정의가 완벽하게 안됐는데 API활용 문서를 보면서 직접 사용해보고 시도해보면서 배울 수 있는 좋은 기회가 되었다.

위치 검색 기능도 구현을 하였는데 카카오 지도 API를 사용해 최상단 검색 결과를 받아오고, 그 받아온 좌표값을 네이버 지도 API를 활용해 마커를 찍어줄 수 있게 하였다. 브라우저에서 현재위치 정보를 받아와 현재위치를 확인할 수 있는 버튼도 만들었다.

### Error

localhost에서 실행시 공공데이터API를 불러오지 못하는 경우가 있는데 이는 브라우저의 CORS 정책 때문이다. 이를 허용해주거나 우회하면 문제없이 API를 사용 할 수 있다.


