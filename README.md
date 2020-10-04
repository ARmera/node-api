# REST API Reference (ARmera)
<br>

* version: 1.0.0
* Servers: http://api.ar.konk.uk/   

건국대학교 졸업프로젝트 ARmera 서버통신 api입니다.<br><br>
<br>   

## /beacon    
| Members | Descriptions |
|:---|:---|
| GET /beacon/ | 전체 비콘 좌표 리스트 조회 |
| GET /beacon/{beacon_id} | 해당 beacon_id 비콘 정보 조회 |
<br>

### GET /beacon/ : 전체 비콘 좌표 리스트 조회 
<br>
 HTTP Result Code가 200 OK일 때 전체 비콘 좌표 리스트를 반환합니다.

 * #### Response   
<br> 

 | Field | Type | Description |
 |:---|:---|:---|
 | id | int | 파라미터로 수신한 비콘의 id |
 | title | string | 비콘의 이름 |
 | latitude | double | 비콘의 경도 |
 | longitude | double | 비콘의 위도 |   
 <br>
 
 #### 성공 예제:
 
 ``` javascript
  [{"id":1,"title":"수의학관","latitude":37.539097,"longitude":127.074711},{"id":2,"title":"공학관","latitude":37.541591,"longitude":127.078893},{"id":3,"title":"인문학관","latitude":37.542436,"longitude":127.078709},{"id":4,"title":"새천년관","latitude":37.543684,"longitude":127.077522},{"id":5,"title":"상허기념도서관","latitude":37.542024,"longitude":127.073852},{"id":6,"title":"법학관","latitude":37.541604,"longitude":127.075089},{"id":7,"title":"황소상","latitude":37.543097,"longitude":127.076151},{"id":8,"title":"와우도","latitude":37.540066,"longitude":127.076585},{"id":9,"title":"산학협동관","latitude":37.54003,"longitude":127.073323},{"id":10,"title":"상허유석창박사동상","latitude":37.54131,"longitude":127.073432},{"id":12,"title":"KU시네마테크","latitude":37.5413385,"longitude":127.0764793},{"id":13,"title":"건국대학교병원","latitude":37.540432,"longitude":127.072298},{"id":14,"title":"건국대학교 기숙사","latitude":37.539296,"longitude":127.077187},{"id":15,"title":"상허유석창박사의묘","latitude":37.540447,"longitude":127.077831},{"id":17,"title":"신공학관","latitude":37.540532,"longitude":127.079462},{"id":18,"title":"이과대학","latitude":37.541479,"longitude":127.080421},{"id":19,"title":"도정궁 경원당","latitude":37.542163,"longitude":127.080389},{"id":20,"title":"경영관","latitude":37.54413,"longitude":127.076368},{"id":24,"title":"학생회관","latitude":37.542205,"longitude":127.077558},{"id":25,"title":"상허연구관","latitude":37.543893,"longitude":127.075482},{"id":26,"title":"행정관","latitude":37.54303,"longitude":127.07531},{"id":29,"title":"상허박물관","latitude":37.542303,"longitude":127.075793},{"id":31,"title":"동물생명과학관","latitude":37.540053,"longitude":127.074401},{"id":32,"title":"생명과학관","latitude":37.541106,"longitude":127.073955},{"id":33,"title":"민주항쟁 동상","latitude":37.543767,"longitude":127.076418}]
 ```   
 <br>
 
### GET /beacon/{beacon_id} : 해당 beacon_id 비콘 정보 조회   
<br>
 HTTP Result Code가 200 OK일 때 해당 beacon_id 비콘 좌표 리스트를 반환합니다.


  * #### Request Parameters   
<br> 

 | Parameter | Type | Description |
 |:---|:---|:---|
 | user_id | | 조회할 사용자 ID |
 
 * #### Response   
<br> 

 | Field | Type | Description |
 |:---|:---|:---|
 | id | int | 파라미터로 수신한 비콘의 id |
 | title | string | 비콘의 이름 |
 | description | string | 비콘에 대한 설명 |
 | stamp | object | 등록 되어있는 스탬프 정보 |
 | latitude | double | 비콘의 경도 |
 | longitude | double | 비콘의 위도 |
 | image_list | array | object detection 이미지 정보 |
 <br>
 
 #### 성공 예제:
 
 ``` javascript
 {"id":1,"title":"수의학관","description":"수의학관에 대한 정보를 입력합니다.","stamp":null,"latitude":37.539097,"longitude":127.074711,"image_list":[]}
 ```

## /image   
| Members | Descriptions |
|:---|:---|
| GET /image/ | 이미지 업로드 페이지 렌더링 |
| GET /image/{image_id} | 해당 image_id 이미지 전송 |
| POST /image/ | 이미지 업로드 |
<br>

### GET /image/ : 이미지 업로드 페이지 렌더링
<br>

이미지를 업로드할 수 있는 페이지를 렌더링합니다.
<br>

### GET /image/{image_id}
<br>
해당 image_id 

  * #### Request Parameters   
<br> 

 | Parameter | Type | Description |
 |:---|:---|:---|
 

## /main   
| Members | Descriptions |
|:---|:---|
| GET /main/weather | 현재 날씨 정보 조회 |
| GET /main/{user_id} | 현재 스탬프 수집 정보 조회 |
<br>

## /route   
| Members | Descriptions |
|:---|:---|
| GET /route/ | 전체 경로 리스트 조회 |
| GET /route/{route_id} | 해당 route_id 경로 정보 조회 |
| POST /route/{route_id} | 투어 시작시 유저의 경로 정보 업데이트 |
| POST /route/{route_id}/complete | 투어 종료시 유저의 경로 정보 업데이트 |
<br>

## /stamp   
| Members | Descriptions |
|:---|:---|
| POST /stamp/ | 스탬프 식별 결과 전송 |
<br>




