Ajax가 적용되지 않은 웹앱: 페이지 전환할때 마다 URL변경, 모든 정보 다운받음.
단지 본문의 부분만을 원해도 굳이 모든 정보를 새로 다운받는다.

Ajax가 적용된 웹앱: 페이지 전환할때 URL 변경 X, 모든 파일을 다운받는게 아니라 내가 요청한 부분만 파일을 다운 받는다 => 시간, 돈, 네트워크 자원 절약, 효율적

Ajax는 보안문제때문에 직접 실행할 수 없고, 웹서버를 통해 구동해야함

fetch('html').then(function(response){ // 서버에게 html이라는 파일 요청
response.text().then(function(text){
alert('text') // 서버가 응답해준 데이터가 text에 저장
})
})

fetch('javascript') => 웹브라우저에게 javascript라는 파일을 서버에 요청
.then: fetch요청이 끝난 후 실행되는 함수 (이름이 없는 익명함수)
Asynchronous: 비동기, 비동기는 동시에 일어나지 X,

response객체
response.status
파일이 정상적으로 작동되면 status = 200
요청한 파일이 존재하지 앟으면 status = 400

해시: 북마크의 개념, 태그에 id를 달아서 사람들이 찾아올 수 있게 만들 수 O.
url#id
fragment: 내용
fragmentIdentifier: fragment를 식별하는 식별자.id
javascript에서 hash 구하기: location.hash

#!html: hash와 구별하기 위해 관습적으로 !를 붙인다.
ajax는 검색엔진에 최적화가 안되어있고 요즘에는 pjax를 쓴다

ajax로 인해 웹은 문서기능 뿐만아니라 애플리케이션의 기능도 갖게 되었다.
Single Page Application - 대표적인 것이 PJAX(pushState + ajax)
Progressive Web Apps - PWA는 SPA의 기반으로 만들어진 앱에 offline에서도 동작하는 기능을 추가했다고 볼 수 O.(online + offline)
