# 개발자가 되기 위해 꼭 알아야 하는 IT 용어

<details>
  <summary> 책 내용 요약 </summary>
    <div markdown="1">
렌더링: 웹 페이지를 구성하는 HTML, CSS 등의 파일을 브라우저상에 그려주는 것
CSR (Client Side Rendering) : 클라이언트 단에서 렌더링을 수행
SSR (Server Side Rendering) : 서버 단에서 렌더링을 수행

캐시: 이전에 사용했던 데이터를 보관하는 사용자의 저장 공간
쿠키: 서버가 사용자에게 저장하는 크기가 작은 문자열 파일
세션: 사용자가 사이트에 로그인 했을 때 일정 기간 동안 서버에서 사용자에 대한 정보를 기록 보관하는 서버의 저장 공간

OSI(Open Systems Interconnection): 개방형 시스템간의 상호 연결
네트워크에서 통신이 일어나는 과정을 7단계로 나눠서 설명한 모델

프로토콜: 네트워크에 연결된 컴퓨터 간에 데이터를 주고받기 위한 약속
HTTP(HyperText Transfer Protocol): 클라이언트와 서버가 리소스를 주고 받기 위해 정해진 규칙

[CORS(Cross-Origin Resource Sharing)] (교차 출처 리소스 공유)
- 기본적으로 브라우저는 보안을 위해 SOP 제한을 하기에 같은 출처에서만 리소스를 공유 할 수 있도록 함.
- 서로 다른 도메인 간의 리소스를 가져오고 싶은 경우, 정해진 규약을 통해 선택한 리소스에 접근 권한을 부여하도록 브라우저에 알려줌.
- CORS는 서버에서 외부 요청을 허용할 때 Ajax 요청이 가능해지는 방식.

[CORS 예시 - Node.js]
- npm i cors
```
var express = require('express')
var cors = require('cors')
var app = express()
 
app.use(cors())
 
app.get('/products/:id', function (req, res, next) {
  res.json({msg: 'This is CORS-enabled for all origins!'})
})
 
app.listen(80, function () {
  console.log('CORS-enabled web server listening on port 80')
})

```

[JSON과 XML]
- 브라우저와 서버 간의 자료를 통신할 때 사용되는 표준화된 데이터 포멧

[SOAP] (Simple Object Access Protocol) 단순 개체 액세스 프로토콜
- SOAP는 웹 서비스에서 사용되는 통신 규약 중 하나입니다. SOAP는 XML 기반의 메시지 교환 프로토콜로, 네트워크 상에서 서로 다른 시스템 간에 데이터를 교환할 때 사용됩니다. SOAP는 보안성이 높고, 다양한 플랫폼에서 사용 가능하며, 대용량 데이터 전송에도 적합합니다.

[VPN] (Virtual Private Network) 가상 사설 통신망
- VPN은 클라이언트와 서버 간의 통신을 암호화하기 때문에 VPN 제공자의 로그를 확인하지 않는 이상 특정 사용자를 추적하기 어렵습니다.

[데이터베이스]
- 공동의 목적을 지닌 다수의 사람이 공유하고 관리하는 데이터의 집합
- 일반적으로 컴퓨터 시스템에 저장되는 구조화된 정보 또는 데이터 집합

[샤딩] (Sharding)
- 데이터베이스 테이블을 조각내어 각각 새로운 노드에 저장하는 데이터 방법
- 데이터가 몰릴 때, 여러 통로를 만들어 트래픽이 몰리는 것을 방지

[ERD] (Entity Relationship Diagram)
- 개체(Entity)들의 관계를 시각적으로 보기 편하게 해 놓은 것

[UML] (Unified Modeling Language)
- 시각적으로 보여주는 설계 다이어그램

[데이터 마이닝]
- 마이닝(mining) : 채굴, 채광
- 데이터 마이닝은 전통적인 데이터 분석 방식으로 찾기 어려운 데이터 내부 패턴, 연관성, 변화와 규칙 같은 중요한 정보를 발견하기 활용하기 위함

[해시]
- 해시는 데이터를 저장하고 검색할 때 사용하는 자료 구조
- 특정한 함수를 사용하여 추출한 값을 활용
- 특정함수 = 입력 된 데이터들끼리 충돌이 발생하지 않게 정리하는 알고리즘

- 해시는 입력 데이터를 고정된 길이의 데이터로 변환한 값
- 데이터의 키 값이 해시 함수를 통해 변환된 간단한 정수

[클라우드]
- 가상 저장 공간 또는 가상화된 컴퓨터의 시스템 리소스(IT 리소스)를 제공하는 것

[git]
- 버전 관리 시스템
- github : 버전관리를 지원하는 웹 서버

[데브옵스] (DevOps)
- 개발과 운영의 합성어 => [빠르게 반복적으로 서비스를 제공하는 역량필요]
- 데브옵스는 비즈니스 측면의 가치를 높이기 위해 개발과 운영의 유기적인 협업을 강조하는 도구, 프로세스, 방법론, 문화, 철학, 전문적 운동 모두를 포괄하는 것이다.
- 데브옵스는 조직의 문화, 사고방식이며 지속적으로 발전하고 개선하는 운동이며, 구성원에게는 일하는 태도이자 습관입니다.

[도커] (Docker)
- 도커는 컨테이너에 다양한 서버의 자원들을 원하는 대로 묶어서 손쉽게 실행하고 배포하는 가상화 플랫폼
- 쉽고 빠른 실행 환경 구성: 원하는 소프트웨어를 묶어서 배포하면 여러 소프트웨어를 설치하지 않고 하나의 이미지로 설치 가능
- 가벼운 용량, 비용 절감 효과: 물리적인 서버는 무겁고 유지 비용이 비쌈. 그에 비해 상대적으로 가볍고 저렴함
- 쉬운 배포: 개발 프로젝트 팀원들이 각자 개발 환경을 구성하면 설정 시 정확성이 떨어지고, 시간이 많이 소요됨. 이때 도커를 사용함.

[쿠버네티스] (Kubernetes)
- 쿠버네티스는 컨테이너화된 애플리케이션을 배포, 관리, 확장할 때 수반되는 다수의 수동 프로세스를 자동화하는 오픈소스 컨테이너 오케스트레이션(Container Orchestration) 도구

[CI/CD] (Continuous Integration / Continuous Deployment)
- 지속적인 통합과 지속적인 배포로서 개발 생산성을 위해 자동화하는 과정
- CI는 미리 코드 검사를 진행할 수 있는 테스팅 코드들을 작성해서 코드에 이상이 있는지 확인하는 작업인 디버깅을 진행하고, 실제 소프트웨어를 공급하는 가공물로 만들어주는 빌드 과정을 자동으로 진행함 (Github Actions)
- CD는 지속적인 배포를 의미. 서버에 하나로 묶은 파일을 올리는 작업을 자동으로 진행.

[CDN] (Contents Delivery Network)
- CDN은 컨텐츠 전송 네트워크를 뜻합니다. 즉, 콘텐츠를 사용자에게 빠르고 안전하게 전달하는 기술. '서버 분산 네트워크'라고도 부르는 CDN은 본 서버의 기능과 데이터를 분산시켜서 지리적 제약 없이 사용자에게 컨텐츠를 제공.
- 원리: 클라이언트가 요청하면 가장 근접한 CDN서버에서 콘텐츠와 데이터를 제공. 본 서버에서는 캐싱을 통해서 CND 서버에 저장함.


  </div>
</details>


---


## 네트워크
<details>
  <summary> TCP와 UDP 차이점을 설명해주세요. </summary>
    <div markdown="1">

TCP는 **Transmission Control Protocol**으로, 전송 제어 프로토콜입니다.<br>
TCP는 신뢰성 있는 데이터 전송을 위해 사용되는 **연결지향 프로토콜**입니다.

UDP는 **User Datagram Protocol**으로 사용자 데이터그램 프로토콜입니다.<br>
UDP는 **빠른 데이터 전송을 중요시**하는 **비연결 프로토콜**입니다.<br>
두 단어 모두에게 존재하는 프로토콜(Protocol)이 디지털 장치간의 서로 통신하고 상호작용하기 위한 규칙의 집합입니다.

**TCP와 UDP의 차이점**은 다음과 같습니다:

**신뢰성**:
- TCP는 데이터 손실이나 순서의 뒤섞임이 발생하지 않습니다.
- UDP는 정확성을 확인하거나 재전송을 요청할 수 없기에 데이터가 손실 되거나 순서가 뒤섞일 수 있습니다.

**연결**:
- TCP는 데이터를 전송하기 전에 연결을 설정하고, 전송 후 연결을 해제합니다. 연결 및 해제과정에서 추가적인 오버헤드는 초래할 수 있으나, 신뢰성 있는 통신을 보장합니다. (오버헤드: 데이터전송 및 처리 과정에서 추가 부담이나 리소스 낭비를 뜻함)
- UDP는 연결 및 해제 단계가 없기에 빠른 전송이 가능하지만 데이터의 무결성을 보장하지 않습니다.

**사용사례**:
- TCP는 주로 이메일, 파일 전송과 같이 신뢰성이 중요한 경우 사용됩니다.
- UDP는 실시간 스트리밍, 온라인 게임, 음성통화 같이 데이터 전송 속도가 중요한 경우 사용됩니다.

![TCP의 3way&4way](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbHoWOZ%2FbtsyQSUDDPR%2FzSvULeIM1LJunmoUVinc4k%2Fimg.png)

"SYN"은 "Synchronize"의 약자로 동기입니다.
"ACK"는 "Acknowledgment"의 약자로 승인입니다.
"FIN"은 "Finish"의 약자로 종료입니다. 그 과정을 리눅스를 통해 3way, 4way인 것이 보입니다.
중간의 P의 경우, 패킷의 약자로 데이터 패킷을 전송하는 과정입니다.

**TCP 패킷의 재전송 과정**:
1. 패킷 송신: 송신자는 여러 개의 패킷으로 나눠 수신자에게 보냄. 각 패킷은 고유한 일련번호를 가지고 있습니다.
2. 패킷 수신: 수신자는 패킷을 받고, 패킷의 일련번호를 확인하여 순서대로 재조립합니다.
3. 패킷 손실 확인: 만약 패킷이 손실되었다고 감지하면, 송신자에게 패킷 손실을 알리기 위한 메시지를 보냅니다.
4. 재전송 요청: 송신자는 손실된 패킷을 재전송하고, 이 패킷의 일련번호를 통해 수신자는 어떤 패킷이 재전송된 것인지 판단할 수 있습니다.
5. 패킷 재전송: 재전송된 패킷은 수신자에게 도착하고 재조립합니다.

**TCP 세션 관리 (연결의 설정과 종료 과정) - Easy Version**:
- 연결 설정 (Handshake): 두 컴퓨터 간의 통신을 먼저 연결 설정해야 합니다. 이 단계를 연결 설정 또는 핸드쉐이크라고 부릅니다.
- 데이터 전송: 연결 설정 후, 데이터를 주고 받을 수 있습니다. A는 작은 조각으로 나눠 B에게 보내면 재조립하여 사용합니다.
- 연결 해제 (Termination): 데이터 통신이 끝난 후, 연결을 해제합니다. A는 B에게 끝내고자 하는 의사를 전달합니다. B는 요청을 수락하고 연결이 종료됩니다.

![TCP의 통신방식](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbaYyaw%2FbtsyPwLxTLK%2FOUwLGVUiHYa0ij2pZNQI8K%2Fimg.png)
- 연결 지향 방식, 패킷 교환방식
- 3way handshaking 으로 연결 4way handshaking으로 해제
- 흐름제어 - 송.수신측의 데이터 처리속도 차이 줄이기 위함, receiver가 현재 상태를 sender에게 피드백해 패킷 수를 조절
- 혼잡 제어 - 송신측의 데이터 전달과 네트워크 데이터 처리 속도 차이를 해결 하기 위함
- 높은 신뢰성- 낮은 성능
- 전이중(각각의 독립된 회선 사용), 점대점(1대1통신) 방식
- 각각의 패킷들은 연결되어있으며 번호가 매겨짐
- 신뢰성있는 전송이 필요할때 사용
- 가변길이 헤더
  
![UDP의 통신방식](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F6tEyH%2FbtsyOFvfD9d%2FvQXKydWBR3KTHCKTRvwZc0%2Fimg.png)
- 비연결형 방식, 데이터그램 방식
- 정보를 주고받을떄 신호절차를 가지고 있지 않음
- UDP헤더의 CheckSum 필드로 최소한의 오류 검출
- 낮은 신뢰성 -높은 성
- 각각의 패킷들은 독립되어있다
- 빠른 전송이 필요할때 사용
- 고정 길이 헤더
- 일반적으로는 저런 내용이지만 UDP는 커스터마이징이 가능하며 개발자의 역량에 따라서 UDP를 이용해 TCP와 비슷한 신뢰성 가지게 할 수 있음 ex) QUIC
  </div>
</details>

<details>
  <summary> RESTful API에 대해 설명해주세요. </summary>
  <div markdown="1">

### REST란?
**REpresentational State Transfer** 의 약자로, 네트워크 상의 Client와 Server 사이의 통신 방식 중 하나입니다. REST는 **자원 (resource)의 표현 (representation)을 통한 상태 전달**을 의미하며, SW에서 관리하는 모든 것을 자원으로 정의하고, 해당 자원의 정보를 주고 받는 방식입니다.

![RESTful API](https://blog.kakaocdn.net/dn/RoRYS/btszvcF6bDZ/sKKc6iCtUTsOJssIOBMsLK/img.png)

#### 정의
- 자원: 해당 SW가 관리하는 모든 것 (문서, 그림, 데이터 등)
- 표현: 그 자원을 표현하기 위한 이름 (예: 학생 정보가 자원이라면 ‘students’ 등)
- 상태 전달: 데이터가 요청되는 시점에 자원의 상태를 전달 (JSON 혹은 XML)

#### 개념
- 어떤 자원에 대해 CRUD 연산을 수행하기 위해 URI (Resource)로 GET, POST 등의 방식 (Method)을 사용하여 요청을 보내면, 요청을 위한 자원은 특정한 형태 (Representation of Resource)로 표현
- URI: Uniform Resource Locator로 인터넷 상 자원의 위치
- URL: Uniform Resource Identifier로 인터넷 상의 자원을 식별하기 위한 문자열의 구성

![URL과 URI](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fcx4Kdb%2FbtszyH50wNO%2FJIyzskvsS9KJTbJmTK0hsK%2Fimg.png)

#### 구성 요소
- 자원 (Resource) - URI
  - 모든 자원에는 고유한 ID가 존재하고, 이 자원은 Server에 존재함
  - 자원을 구별하는 ID는 '/exgroups/:exgroup_id'와 같은 HTTP URI 임
  - Client는 URI를 이용해 자원을 지정하고 해당 자원의 상태(정보)에 대한 조작을 Server에 요청
- 행위 (Verb) - Method
  - HTTP 프로토콜의 Method(GET, POST, PUT, PATCH, DELETE)를 사용
- 표현 (Representation of Resource)
  - Client와 Server가 데이터를 주고받는 형태로 JSON, XML, TEXT, RSS 등이 있음
  - JSON, XML을 통해 데이터를 주고 받는 것이 일반적
- Server-Client (서버-클라이언트 구조)
  - 자원이 있는 쪽이 Server, 자원을 요청하는 쪽이 Client가 됩니다.
  - REST Server: API를 제공하고 비즈니스 로직 처리 및 저장을 책임집니다.
  - Client: 사용자 인증이나 context(세션, 로그인 정보) 등을 직접 관리하고 책임집니다.
  - 서로 간 의존성이 줄어듭니다.

#### Stateless (무상태)
- HTTP 프로토콜은 Stateless Protocol이므로 REST 역시 무상태성을 가집니다.
- Client의 context를 Server에 저장하지 않음
- 세션과 쿠키와 같은 context 정보를 신경쓰지 않아도 되므로 구현이 단순화됩니다.
- Server는 각각의 요청을 완전히 별개의 것으로 인식하고 처리
- 각 API 서버는 Client의 요청만을 단순 처리
- 이전 요청이 다음 요청의 처리에 연관되어서는 안 됨
- 물론 이전 요청이 DB를 수정하여 DB에 의해 바뀌는 것은 허용
- Server의 처리 방식에 일관성을 부여하고 부담이 줄어들며, 서비스의 자유도가 높아집니다.

#### Cacheable (캐시 처리 가능)
- 웹 표준 HTTP 프로토콜을 그대로 사용하므로 웹에서 사용하는 기존의 인프라를 그대로 활용 가능
- HTTP가 가진 가장 강력한 특징 중 하나인 캐싱 기능을 적용할 수 있음
- HTTP 프로토콜 표준에서 사용하는 Last-Modified 태그나 E-Tag를 이용하면 캐싱 구현이 가능
- 대량의 요청을 효율적으로 처리하기 위해 캐시가 요구됨
- 캐시 사용을 통해 응답 시간이 빨라지고 REST Server 트랜잭션이 발생하지 않기 때문에 전체 응답 시간, 성능, 서버의 자원 이용률을 향상시킬 수 있음

#### Layered System (계층화)
- Client는 REST API Server만 호출
- REST Server는 다중 계층으로 구성될 수 있음
- API Server는 순수 비즈니스 로직을 수행하고 그 앞단에 보안, 로드 밸런싱, 암호화, 사용자 인증 등을 추가하여 구조상의 유연성을 제공
- 로드 밸런싱, 공유 캐시 등을 통해 확장성과 보안성을 향상시킬 수 있음
- PROXY, 게이트웨이 같은 네트워크 기반의 중간 매체를 사용할 수 있음

#### Code-On-Demand (optional)
- Server로부터 스크립트를 받아서 Client에서 실행
- 반드시 충족할 필요는 없음

#### Uniform Interface (인터페이스 일관성)
- URI로 지정한 Resource에 대한 조작을 통일되고 한정적인 인터페이스로 수행
- HTTP 표준 프로토콜에 따르는 모든 플랫폼에서 사용이 가능
- 특정 언어나 기술에 종속되지 않음

#### 설계 기본 규칙
- URI는 자원을 표현해야함
- 동사보다는 명사, 대문자보다는 소문자 이용
- 도큐먼트 이름 = 단수 명사 이용
- 컬렉션 이름 = 복수 명사 이용
- 스토어 이름 = 복수 명사 이용
- 자원에 대한 행위는 HTTP Method로 표현
- URI에 Method가 들어가면 안됨
- URI에 행위에 대한 동사 표현이 들어가면 안됨
- 경로 부분 중 변하는 부분은 유일 값으로 대체함 (예: id)
- 마지막 문자로 / 를 넣지 않음
- 불가피하게 긴 경로를 사용할 경우 (-)을 사용해 가독성을 높이며 (_)은 이용하지 않음
- 확장자는 URI에 포함하지 않음

#### REST 아키텍처 스타일을 따르는 API
- REST API

#### REST 아키텍처를 완전하게 따라 만들어진 API
- RESTful API

#### REST 아키텍처를 구현하는 웹 서비스
- RESTful 웹 서비스

#### 예시 코드
```javascript
const express = require('express');
const app = express();
app.use(express.json());

let books = [
  { id: 1, title: 'Book 1', author: 'Author 1'},
  { id: 2, title: 'Book 2', author: 'Author 2'},
  { id: 3, title: 'Book 3', author: 'Author 3'}
];

app.get('/books', (req, res) => {
  res.json(books);
});

app.get('/books/:id', (req, res) => {
  const book = books.find(b => b.id === parseInt(req.params.id));
  if (!book) res.status(404).send('The book with the given ID was not found.');
  res.send(book);
});

app.post('/books', (req, res) => {
  const book = {
    id: books.length + 1,
    title: req.body.title,
    author: req.body.author
  };
  books.push(book);
  res.send(book);
});

app.put('/books/:id', (req, res) => {
  const book = books.find(b => b.id === parseInt(req.params.id));
  if (!book) res.status(404).send('The book with the given ID was not found.');

  book.title = req.body.title;
  book.author = req.body.author;

  res.send(book);
});

app.delete('/books/:id', (req, res) => {
  const book = books.find(b => b.id === parseInt(req.params.id));
  if (!book) res.status(404).send('The book with the given ID was not found.');

  const index = books.indexOf(book);
  books.splice(index, 1);

  res.send(book);
});

const port = process.env.PORT || 3000;
app.listen(port, () => console.log(`Listening on port ${port}...`));
```

# REST 아키텍처 원칙에 따른 API 구현

이 코드는 **REST 아키텍처 원칙**을 따르는 API를 구현하고 있습니다. RESTful API의 핵심 원칙은 **자원(Resource)**, **행위(Verb)**, **표현(Representation)** 입니다.

## 자원(Resource)

이 코드에서 자원은 **책(Book)** 입니다. 각 책은 고유한 ID를 가지며, 이를 통해 책을 식별하고 접근할 수 있습니다.

## 행위(Verb)

HTTP 메서드(GET, POST, PUT, DELETE)를 사용하여 책에 대한 CRUD 연산을 수행합니다.

- `GET /books`: 모든 책의 목록을 가져옵니다.
- `GET /books/:id`: 특정 ID의 책을 가져옵니다.
- `POST /books`: 새로운 책을 추가합니다.
- `PUT /books/:id`: 특정 ID의 책 정보를 업데이트합니다.
- `DELETE /books/:id`: 특정 ID의 책을 삭제합니다.

## 표현(Representation)

클라이언트와 서버가 데이터를 주고받는 형태입니다. 이 코드에서는 **JSON 형식**으로 데이터를 주고받습니다.

또한, 이 코드는 **Stateless(무상태성) 원칙**도 따르고 있습니다. 각 요청은 독립적으로 처리되며, 서버는 클라이언트의 상태 정보를 저장하지 않습니다. 따라서 이 코드는 REST 아키텍처 원칙에 따라 설계된 API입니다. 이러한 방식은 클라이언트와 서버 간의 상호작용을 단순화하고, 확장성과 유연성을 제공합니다. 이것이 위의 코드가 RESTful API로 설계된 이유입니다.


  </div>
</details>

<details>
  <summary> "https://www.google.com/" 접속 시 일어나는 네트워크 과정 </summary>
    <div markdown="1">

유저가 브라우저에 google.com을 치면 다음과 같이 상황이 발생합니다.

### 1. 브라우저 캐시 체크
일단 브라우저는 캐시를 확인합니다. 

첫 번째로, 기존에 구글에 방문했다면 구글에 빠르게 접근할 수 있는 '브라우저 캐시'를 확인합니다.

두번째, 운영체제 안에 있는 캐시인 'OS캐시'를 확인합니다. 

세번째, 집안에 있는 공유기에 있는 '라우터 캐시'를 확인합니다.

마지막으로 인터넷을 제공하는 회사의 ISP(Internet Service Provider)캐시를 확인합니다.

### 2. DNS(Domain Name Service)로 IP 주소 획득
마지막 ISP 캐시에서까지 IP주소를 찾을 수 없었다면, 이제 ISP의 DNS server에 DNS 쿼리를 보내야 합니다. 

즉, "구글이라는 IP주소를 나한테 알려줘"라고 물어보는 겁니다. 다음의 그림과 같은 과정을 거칩니다.

![DNS](https://webhostinggeeks.com/guides/dns/structure2.png)

위의 내용을 설명하자면,
Root Domain에 연락 -> Top-level Domain인 .com NDS 연락 ->
Second-level domain인 google.com 네임서버로 이동 ->
구글에서 www의 ip address를 DNS recursor에 보냄
결국 google.com의 IP 주소를 찾게 됩니다.

### 3. 브라우저가 TCP/IP 프로토콜을 사용해 서버에 연결

이제 IP주소를 알았기에, TCP(Transmission Control Protocol)/IP(Internet Protocol)을 이용하여 서버에 연결하려고 신호를 보냅니다. 

![TCP의 3way&4way](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbHoWOZ%2FbtsyQSUDDPR%2FzSvULeIM1LJunmoUVinc4k%2Fimg.png)

TCP연결은 위와 같은 그림을 통해 연결합니다. 그중에서 연결하는 과정은
3way handshaking이라고 합니다. 이를 통해 서로 안전하게 정보를 연결합니다.

### 4. Firewall & Https/SSL

TCP 연결을 하는 중, Firewall과 https나 SSL이라고 하는 접근 제한 방법이 있습니다. Firewall은 불이 났을 때, 공기를 차단하는 벽처럼, 인터넷에서도 해커가 무자비한 서비스 트래픽을 보내는 경우를 대비해 **Firewall**을 설치해, **특정 IP주소나 어떤 지역에서 접근해 오는 신호를 차단**할 수 있습니다.

**Https/SSL은 클라이언트와 서버와의 암호화를 통해 중간에 누가 패킷을 엿듣는 것을 차단**합니다. 

**SSL**은 **웹사이트와 브라우저 사이**에 **전송되는 데이터를 암호화**하여 **인터넷 연결을 보호**하기 위한 **표준 기술**입니다. **SSL은 공개키 암호화 방식**을 사용합니다. 이 방식은 데이터를 암호화하는 공개키와 데이터를 복호화하는 개인키를 사용합니다. 이를 통해 데이터를 안전하게 전송할 수 있습니다.

### 5. Load balancer

많은 사람들이 서버에 접속한다면 과부하가 걸릴 겁니다. 여러대의 서버를 가지고
Load balancer를 통해 트래픽을 잘 측정하여, 트래픽을 받을 수 있는 서버로 보냅니다.

### 6. 웹서버

TCP 연결이 된 후 이제 클라이언트는 데이터를 보내고,
해당 데이터에는 "나에게 첫 페이지를 보내줘"라는 신호와 함께 보내집니다.

여기에는 브라우저 버전과 종류, 쿠키(사용자 정보) 등의 내용이 함께 보내지며,
구글은 여기서 사용자에게 필요한 내용을 요청한 방식으로 보내주게 됩니다.

### 7. HTML 컨텐츠 렌더링

이제 브라우저는 구글 서버에서 받은 HTTP코드와 HTML을 통해 렌더링을 시작하며, 필요한 이미지나 다른 파일들이 있으면, 또 보내달라고 요청을 하며, 사용자는 구글의 페이지를 보게 됩니다.

**여기까지가 google.com을 입력했을 때 이뤄지는 일이었습니다!**

  </div>
</details>

<details>
  <summary> HTTP와 HTTPS의 차이점은 무엇인가요? </summary>
    <div markdown="1">

**HTTP**(Hypertext Transfer Protocol)는 **클라이언트와 서버 간 통신을 위한 통신 규칙** 또는 **프로토콜**입니다. 사용자가 웹 사이트를 방문하면 사용자 브라우저가 웹 서버에 HTTP 요청을 전송하고 웹 서버는 HTTP 응답으로 응답합니다. 웹 서버와 사용자 브라우저는 데이터를 일반 텍스트로 교환합니다. 간단히 말해 **HTTP 프로토콜은 네트워크 통신을 작동하게 하는 기본 기술입니다.**

이름에서 알 수 있듯이 **HTTPS**(Hypertext Transfer Protocol **Secure**)는 HTTP의 확장 버전 또는 더 안전한 버전입니다. HTTPS에서는 브라우저와 서버가 **데이터를 전송하기 전에 안전하고 암호화된 연결을 설정**합니다.

HTTPS는 **SSL(Secure Socket Layer)** 프로토콜을 이용하여 **데이터를 암호화**합니다. 이를 통해 데이터를 전송하는 과정에서 중간에 제3자가 데이터를 가로채더라도 데이터를 해독할 수 없습니다.

**SSL**은 **웹사이트와 브라우저 사이**에 **전송되는 데이터를 암호화**하여 **인터넷 연결을 보호**하기 위한 **표준 기술**입니다. **SSL은 공개키 암호화 방식**을 사용합니다. 이 방식은 데이터를 암호화하는 공개키와 데이터를 복호화하는 개인키를 사용합니다. 이를 통해 데이터를 안전하게 전송할 수 있습니다.

HTTPS를 사용하면, 사용자가 웹사이트에 로그인하거나 개인정보를 입력하는 등의 작업을 할 때, 제3자가 정보를 가로채어 악용하는 것을 방지할 수 있습니다.

  </div>
</details>

<details>
  <summary> HTTPS와 SSL Handshake에 대해 설명해보세요. </summary>
    <div markdown="1">

**HTTPS**는 HTTP 프로토콜에 **보안 계층을 추가한 것**입니다. 
**SSL(Secure Sockets Layer)** 는 보안용 프로토콜에 사용되는 암호화 기술입니다. 

**SSL Handshake**는 SSL/TLS 프로토콜에서 사용되는 과정으로, **클라이언트와 서버 간의 보안 연결을 설정하는 과정**입니다.

1. 클라이언트가 서버에 접속하면, 서버는 클라이언트에게 공개키를 전송합니다.
2. 클라이언트는 이 공개키를 사용하여 랜덤한 대칭키를 암호화하여 서버에 전송합니다.
3. 서버는 이 암호화된 대칭키를 자신의 개인키를 사용하여 복호화합니다.
4. 이후 클라이언트와 서버는 이 대칭키를 사용하여 암호화된 통신을 수행합니다.

이러한 보안 프로토콜은 인터넷 상에서 데이터를 안전하게 전송하기 위해 필수적입니다.

  </div>
</details>

<details>
  <summary> GET과 POST의 차이점에 대해서 설명해보세요. </summary>
    <div markdown="1">

HTTP 프로토콜에서 GET과 POST는 두 가지 주요한 요청 방식입니다. 
GET은 **서버로부터 데이터를 요청**하는 데 사용되며, **URL에 쿼리 문자열을 포함**합니다. 
반면, POST는 **서버에 데이터를 제출하는 데 사용**되며, **HTTP 요청의 본문에 데이터를 포함**합니다.

GET과 POST의 차이점은 다음과 같습니다:

- GET 요청에서는 URL에 쿼리 문자열을 포함하여 데이터를 전송합니다. 반면, POST 요청에서는 HTTP 요청의 본문에 데이터를 포함하여 전송합니다. 예를 들어, GET 요청에서는 https://example.com/search?q=apple과 같이 URL에 데이터를 포함하여 검색 결과를 요청할 수 있습니다. 반면, POST 요청에서는 HTTP 요청의 본문에 데이터를 포함하여 로그인 정보나 회원가입 정보 등을 서버에 제출할 수 있습니다.
- GET 요청은 북마크할 수 있지만, POST 요청은 북마크할 수 없습니다. 이는 GET 요청에서는 URL에 데이터가 포함되어 있어 북마크를 통해 다시 접속하면 동일한 데이터를 요청할 수 있기 때문입니다. 반면, POST 요청에서는 URL에 데이터가 포함되어 있지 않아 북마크를 통해 다시 접속하면 동일한 데이터를 제출할 수 없습니다.
- GET 요청은 URL 길이 제한이 있습니다. 반면, POST 요청은 데이터 길이에 대한 제한이 없습니다.
- GET 요청은 데이터를 요청하는 데 사용되며, 데이터를 수정하지 않습니다. 반면, POST 요청은 데이터를 생성하거나 수정하는 데 사용됩니다.

PUT, DELETE, HEAD, OPTIONS, CONNECT, TRACE 등의 다른 HTTP 메서드도 있지만, GET과 POST가 가장 많이 사용됩니다.

참고로, GET 요청은 민감한 데이터를 다룰 때 사용해서는 안 됩니다.
이유는 GET요청은 쿼리 문자열은 URL에 노출되어 보안상 취약하고 브라우저에 기록을 남기기 때문입니다.

  </div>
</details>

<details>
  <summary> HTTP 메서드 정의와 역할에 대해서 설명해보세요. </summary>
    <div markdown="1">

**HTTP(HyperText Transfer Protocol)**는 클라이언트와 서버 간의 통신을 위한 프로토콜입니다.

**HTTP 요청 메서드**는 **주어진 리소스에 수행하길 원하는 행동을 나타냅니다.**

각각의 메서드는 서로 다른 의미를 구현하지만, 일부 기능은 메서드 집합 간에 서로 공유하기도 합니다.

이를테면, GET 메서드는 특정 리소스의 표시를 요청하고, POST 메서드는 특정 리소스에 엔티티를 제출할 때 쓰입니다.

HTTP 요청 메서드는 다음과 같습니다:

- GET: 특정 리소스의 표시를 요청합니다. GET을 사용하는 요청은 오직 데이터를 받기만 합니다.
- POST: 특정 리소스에 엔티티를 제출할 때 쓰입니다. 이는 종종 서버의 상태의 변화나 부작용을 일으킵니다.
- PUT: 목적 리소스 모든 현재 표시를 요청 payload로 바꿉니다.
- PATCH: 리소스의 부분만을 수정하는 데 쓰입니다.
- DELETE: 특정 리소스를 삭제합니다.

---

- HEAD: GET 메서드의 요청과 동일한 응답을 요구하지만, 응답 본문을 포함하지 않습니다.
- CONNECT: 목적 리소스로 식별되는 서버로의 터널을 맺습니다.
- OPTIONS: 목적 리소스의 통신을 설정하는 데 쓰입니다.
- TRACE: 목적 리소스의 경로를 따라 메시지 loop-back 테스트를 합니다.

**HTTP 요청 메서드는 클라이언트가 서버에게 요청을 보낼 때 사용됩니다.** 이를테면, GET 메서드를 사용하여 웹 페이지를 요청하면, 서버는 해당 페이지의 HTML 코드를 응답으로 보내줍니다. 이와 같이, HTTP 요청 메서드는 클라이언트와 서버 간의 통신을 가능하게 합니다.

  </div>
</details>

<details>
  <summary> CORS란 무엇인지 설명해주세요. </summary>
    <div markdown="1">

**CORS**는 "Cross-Origin Resource Sharing"의 약자로, **웹에서 다른 출처(도메인, 프로토콜, 포트)의 자원에 접근할 수 있도록 하는 보안 메커니즘**입니다.

- "Cross-Origin Resource Sharing"을 합쳐서 해석하면, "다른 출처(Origin)의 자원(Resource)을 웹 페이지에서 공유(Sharing)할 수 있도록 허용하는 것”

간단하게 말해서, **웹 페이지는 기본적으로 같은 출처에서만 데이터를 불러오도록 제한**되어 있습니다. 이는 보안상의 이유 때문인데, 다른 출처에서 스크립트나 데이터를 불러오는 것이 허용되면 해커들이 악의적인 코드를 심을 수 있기 때문입니다.

그런데 웹 개발을 하다 보면 때때로 다른 출처의 데이터나 자원이 필요한 경우가 있습니다. 예를 들어, 당신이 만든 웹사이트가 [](http://mywebsite.com/)[http://mywebsite.com](http://mywebsite.com) 이고, 당신이 다른 사이트 [](http://api.othersite.com/)[http://api.othersite.com](http://api.othersite.com) 에서 제공하는 데이터를 사용하고 싶을 때입니다. 이**때 CORS 정책이 없다면 보안상의 이유로 이러한 요청은 차단**됩니다.

CORS는 이러한 문제를 해결하기 위해 만들어졌습니다. **서버에서 특정 HTTP 헤더를 설정하면, 브라우저는 이를 감지하고 다른 출처의 자원에 대한 접근을 허용하게 됩니다.**

즉, **CORS는 안전한 방법으로 다른 출처의 자원을 사용할 수 있게 해주는 규칙이자 시스템**이라고 할 수 있습니다.

다음은 node.js에서 cors를 사용하는 간단한 예시 코드

```jsx
// npm install express cors

---

const express = require('express');
const cors = require('cors');

const app = express();

// CORS 미들웨어를 사용하여 모든 요청에 대해 CORS를 허용합니다.
app.use(cors());

// 예시 라우트
app.get('/data', (req, res) => {
    res.json({ message: 'Hello World' });
});

// 서버를 3000 포트에서 실행합니다.
app.listen(3000, () => {
    console.log('Server running on port 3000');
});
```

  </div>
</details>

<details>
  <summary> OSI7계층과 TCP/IP 4계층에 대해 설명해보세요. </summary>
    <div markdown="1">

**OSI 7계층**은 **통신이 일어나는 과정을 7개의 계층**으로 나눈 모델입니다.

이 모델은 통신 과정을 단계별로 파악할 수 있어 흐름을 한눈에 알아보기 쉽고, 사람들이 이해하기 쉽습니다. 또한, 7단계 중 특정한 곳에 이상이 생기면 다른 단계 장비, 소프트웨어를 건들이지 않고 이상이 생긴 단계만 고칠 수 있습니다.

**TCP/IP 4계층**은 OSI7계층과 달리 좀 더 **실무적이면서 프로토콜 중심으로 단순화된 모델**입니다. TCP/IP 4계층은 현재 **인터넷에서 사용되는 프로토콜로, 데이터 통신을 4개의 계층**으로 나누어 구성합니다.

TCP/IP 4계층의 구성은 다음과 같습니다:

1. **애플리케이션 계층**: HTTP, FTP, SMTP 등의 프로토콜이 사용됩니다.
2. **전송 계층**: TCP 프로토콜이 사용됩니다.
3. **네트워크 계층**: IP 프로토콜이 사용됩니다.
4. **데이터 링크 계층**: 이더넷 프로토콜이 사용됩니다.

TCP/IP 4계층은 OSI7계층과 달리 프로토콜 중심으로 단순화된 모델이기 때문에, OSI7계층보다 좀 더 실무적으로 사용됩니다.

  </div>
</details>

---

## 운영체제

<details>
<summary> 멀티프로세스와 멀티스레드에 대해 설명해주세요. </summary>
<div markdown="1">

![멀티프로세스VS멀티스레드](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcLeuBN%2FbtszzIFjtP3%2FVtysBpPVKh53hqbmWx0uZ1%2Fimg.png)
 
 **개인적으로 멀티프로세스와 멀티스레드를 한방에 이해 시켜준 이미지**
 **멀티 프로레스(크롬) VS 멀티 스레드 (익스플로어)**

![프로세스](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fc9FvPh%2FbtszzKb8NMM%2FMTZoVCWQ2VBMa9YN0eP4kk%2Fimg.png)
![작업관리](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FBP5ib%2FbtszC4UrBxh%2FOh5yPSfE9jKveFJsCCEXb0%2Fimg.png)

**프로세스는 운영체제로부터 자원을 할당받는 작업의 단위**

<br>

**프로세스의 특징**
- 프로세스는 각각 독립된 메모리 영역(Code, Data, Stack, Heap의 구조)을 할당받는다.
- 기본적으로 프로세스당 최소 1개의 스레드(메인 스레드)를 가지고 있다. 각 프로세스는 별도의 주소 공간에서 실행되며, 한 프로세스는 다른 프로세스의 변수나 자료구조에 접근할 수 없다.
- 한 프로세스가 다른 프로세스의 자원에 접근하려면 프로세스 간의 통신(IPC, inter-process communication)을 사용해야 한다. Ex. 파이프, 파일, 소켓 등을 이용한 통신 방법 이용

| 항목 | 프로그램 | 프로세스 |
| --- | --- | --- |
| 정의 | 어떤 작업을 하기 위해 실행할 수 있는 파일 | 실행되어 작업 중인 컴퓨터 프로그램 |
| 상태 | 파일이 저장 장치에 있지만 메모리에는 올라가 있지 않은 정적인 상태 | 메모리에 적재되고 CPU 자원을 할당받아 프로그램이 실행되고 있는 상태 |
| 요약 | 그냥 코드 덩어리 | 그 코드 덩어리를 실행한 것 |

![스레드](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbbcJ4D%2FbtszCeQ2sD7%2FMpytRcp7gKqafJCwTmXek1%2Fimg.png)

**스레드는 프로세스가 할당받은 자원을 이용하는 실행의 단위 (= 프로세스 내에서 실행되는 여러 흐름의 단위)**

<br>

**스레드의 특징**
- 스레드는 프로세스 내에서 각각 Stack만 따로 할당받고 Code, Data, Heap 영역은 공유한다.
- 스레드는 한 프로세스 내에서 동작되는 여러 실행의 흐름으로, 프로세스 내의 주소 공간이나 자원들(힙 공간 등)을 같은 프로세스 내에 스레드끼리 공유하면서 실행된다.
- 각각의 스레드는 별도의 레지스터와 스택을 갖고 있지만, 힙 메모리는 서로 읽고 쓸 수 있다.
- 한 스레드가 프로세스 자원을 변경하면, 다른 이웃 스레드(sibling thread)도 그 변경 결과를 즉시 볼 수 있다.

<br>
<br>

#### 멀티프로세스와 멀티스레드
**멀티 프로세싱 (Multiprocessing)은 다수의 프로세서로 다수의 "프로세스"를 협력적으로 동시에 처리하는 것입니다.** 
<br>

**멀티스레딩 (Multithreading)은 하나의 프로세스 안에서 여러 개의 실행 흐름 (스레드)을 두는 방식으로 여러 실행을 동시에 실행하도록 하나의 프로세스를 운영하는 방식입니다.**

![멀티프로세스VS멀티스레드](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcLeuBN%2FbtszzIFjtP3%2FVtysBpPVKh53hqbmWx0uZ1%2Fimg.png)

### [크롬]

**멀티 프로세스의 장점**
1. 안정성 : 하나의 프로세스가 죽어도 다른 프로세스에 영향을 미치지 않습니다.
2. 보안: 각 프로세스는 자신의 메모리 공간을 가지고 있어 다른 프로세스의 메모리에 접근할 수 없습니다.
<br>

**멀티 프로세스의 단점**
1. 시스템 자원 소모: 각 프로세스는 자신만의 메모리 공간을 가지므로, 메모리를 많이 소모합니다.
2. IPC(Inter-Process Communication)가 필요합니다.

<details>
<summary>IPC(프로세스 간 통신)</summary>

IPC(Inter-Process Communication)가 필요한 이유를 멀티프로세스의 단점으로 볼 수 있는 주요 이유는 다음과 같습니다:

- 복잡성: IPC는 프로세스 간에 데이터를 전송하고 동기화하는 복잡한 메커니즘이 필요합니다. 이로 인해 프로그램의 설계와 구현이 복잡해질 수 있습니다.
- 성능 저하: IPC를 통한 데이터 전송은 프로세스 내부에서 데이터를 전송하는 것보다 더 많은 시간과 자원을 소모합니다. 따라서, IPC를 많이 사용하는 멀티프로세스 시스템은 성능 저하를 경험할 수 있습니다.
- 동기화 문제: 여러 프로세스가 동시에 같은 자원에 접근하려고 할 때 발생하는 동기화 문제를 해결하기 위해 추가적인 메커니즘이 필요합니다. 이는 프로그램의 복잡성을 더욱 증가시키며, 잘못 관리되면 데이터 불일치와 같은 문제를 초래할 수 있습니다.

따라서, IPC가 필요한 멀티프로세스 시스템은 이러한 단점들로 인해 개발 및 유지보수가 어렵고, 성능 저하를 경험할 수 있습니다. 이러한 이유로 IPC의 필요성을 멀티프로세스의 단점으로 볼 수 있습니다.

</details>


### [익스플로어]

**멀티 스레드의 장점**
1. 시스템 자원 소모가 적습니다.
2. IPC가 필요하지 않습니다.
   
<br>

**멀티 프로세스의 단점**
1. 안정성: 하나의 스레드가 죽으면 전체 프로세스가 영향을 받습니다.
2. 보안: 각 스레드는 자신이 속한 프로세스의 메모리 공간을 공유하므로, 다른 스레드가 메모리에 접근할 수 있습니다.

</div>
</details>

---

## 데이터베이스
<details>
<summary> 트랜잭션과 격리 수준에 대해 설명해주세요. </summary>
<div markdown="1">

#### 정의
**트랜잭션(Transaction)** 은 **데이터베이스의 상태를 변환시키는 하나의 논리적 기능을 수행하기 위한 작업의 단위** 또는 **한꺼번에 모두 수행되어야 할 일련의 연산** 들을 의미합니다.

```
// 트랜잭션 시작
BEGIN TRAN

//변경할 쿼리문
UPDATE tbl_admin
SET nickname = "babo"
WHERE no= 1;

//결과 확인해 본 후
select * from tbl_admin

//성공 처리
COMMIT TRAN
//실패 처리
ROLLBACK TRAN
```

이론공부만 하던 시절에는 와닿지 않았던 개념이었는데, 현업에서 사용하게 되어서 CS의 주제로 선정하게 되었다.
위의 쿼리문 처럼 변경을 시작하기 전에 **" BEGIN TRAN "** 을 실행하고, **변경하는 쿼리문** 을 실행한다.
잘 변경되었나 확인해보고, 잘 못 변경되었다면 **ROLLBACK**, 잘 되었다면 **COMMIT**을 실행시킨다.

#### 주요목적

**트랜잭션의 주요 목적**은 **데이터의 무결성과 일관성을 보장**하는 것입니다. 여러 작업을 단일 트랜잭션으로 그룹화하여 트랜잭션 내의 모든 작업이 성공적으로 실행되거나 아무 것도 실행되지 않도록 할 수 있습니다.

<br>

**트랜잭션**은 신뢰할 수 있고 일관된 데이터 처리를 보장하는 **ACID속성**을 따릅니다. 트랜잭션은 원자성(Atomicity), 일관성(Consistency), 독립성(Isolation), 지속성(Durability)의 4가지 특징을 가집니다.

1. 원자성은 트랜잭션이 데이터베이스에 모두 반영되던가, 아니면 전혀 반영되지 않아야 한다는 것을 의미
2. 일관성은 트랜잭션의 작업 처리 결과가 항상 일관성이 있어야 한다는 것을 의미
3. 독립성은 둘 이상 트랜잭션이 동시 실행시, 어떤 트랜잭션이라도 다른 트랜잭션 연산에 끼어들 수 없다는 점을 의미
4. 지속성은 트랜잭션이 성공적으로 완료됬을 경우, 결과는 영구적으로 반영되어야 한다는 점

<br>

[ "트랜잭션에서 ACID 속성을 따른다"는 것은 원자성, 일관성, 독립성, 지속성을 최대한 지키려고 노력한다는 것을 의미"]

#### 트랜잭션의 격리수준 4단

- 트랜잭션 **격리수준(isolation level)** 이란 **동시에 DB에 접근할 때, 그 접근을 어떻게 제외할지에 대한 설정**
- 동시에 여러 트랜잭션이 처리될 때, 트랜잭션끼리 얼마나 서로 고립되어 있는지를 나타내는 것. **즉, 특정 트랙잭션이 다른 트랜잭션이 변경한 데이터를 볼 수 있도록 허용할지 말지를 결정하는 것**

#### 격리 수준 단계
1. READ UNCOMMITED
2. READ COMMITED
3. REPEATABLE READ
4. SERIALIZABLE
<br>
- 격리 수준 증가할 수록 일관성은 증가하지만 동시성은 감소
- 일반적인 DB 서비스는 READ COMMITED 또는 REPEATABLE READ 중 하나를 선택(oracle = READ COMMITED, mysql = REPEATABLE READ)

### 1. READ-UNCOMMITED

![READ-UNCOMMITED](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fbtm4xu%2FbtszKdwy2Ra%2FfDbkMxXUb4TP8UT61tz3Y1%2Fimg.png)

- 변경사항을 커밋하기 전에 다른 트랜잭션에서 조회할 수 있는 수준 (일반적으로 사용되지 않음)

- Dirty Read, Repeatable Read, Phantom Read 문제도 발생할 수 있음.

### 2. READ-COMMITED

![READ-COMMITED](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FwmHZD%2FbtszHH6gDv5%2F4aEpAlMuXZkkgxrtYxn19K%2Fimg.png)

- 어떤 트랜잭션의 변경내용이 커밋이 완료된 데이터만 다른 트랜잭션에서 조회 가능. 트랜잭션이 이루어지는동안 다른 사용자는 해당 데이터에 접근이 불가능.

- 커밋전에 조회가 됨으로 VALUE(값)의 오류가 발생할 수 있음

- 이 격리수준은 Oracle DBMS 에서 기본으로 사용하고 있으며, 대중적으로 가장 많이 선택되는 격리수준

- 결제 기능과 같은 금전적인 처리와 연결된 기능이라면 문제가 발생할 수 있음

-  ‘Dirty Read’ 문제는 해결, 'Non-Repeatable Read’와 ‘Phantom Read’ 문제는 발생할 수 있음.


### 3. REPETABLE READ

![REPETABLE READ](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FLYt9e%2FbtszF2p0mbv%2FiKPfx7Df23KOYXbTDxMYTK%2Fimg.png)


- 트랜잭션이 시작되기 전에 커밋된 내용에 대해서만 조회할 수 있는 격리수준. 트랜잭션이 완료될 때 까지 SELECT 쿼리가 사용되는 모든 데이터에 Shared Lock(공유 락)이 걸리는 계층. (VALUE의 오류가 발생할 수 없음)

- 원래 존재하지 않았던 컬럼이 조회될 수 있음 (Phantom Read)

- 대신 나머지 현상 사라짐

### 4. SERIALIZABLE

- 한 트랜잭션에서 사용하는 데이터를 다른 트랜잭션에서 절대 접근할 수 없음.

- 트랜잭션의 ACID 성질이 엄격하게 지켜지지만, 성능은 가장 떨어짐.

- 트랜잭션이 완료될때까지 SELECT 쿼리가 사용되는 모든 데이터에 Shared Lock(공유 락) 이 걸리는 계층

- 가장 엄격한 격리수준으로, 완벽한 읽기 일관성 모드를 제공한다.

- 다른 사용자는 트랜잭션 영역에 해당되는 데이터에 대한 수정 및 입력 불가능

#### 격리수준에서 발생하는 문제

- Dirty Read: 이는 한 트랜잭션이 아직 커밋되지 않은 다른 트랜잭션의 변경 사항을 읽는 현상을 말합니다. 예를 들어, 한 트랜잭션이 데이터를 수정했지만 아직 커밋하지 않았는데, 다른 트랜잭션이 그 변경 사항을 읽는 경우를 말합니다. 이로 인해 데이터의 일관성이 깨질 수 있습니다.
- Non-Repeatable Read: 이는 한 트랜잭션이 동일한 데이터를 두 번 읽었을 때, 그 사이에 다른 트랜잭션이 해당 데이터를 수정하고 커밋하여 두 번째 읽기에서 다른 결과를 얻는 현상을 말합니다. 이로 인해 한 트랜잭션 내에서 데이터의 일관성이 깨질 수 있습니다.
- Phantom Read: 이는 한 트랜잭션이 동일한 쿼리를 두 번 실행했을 때, 그 사이에 다른 트랜잭션이 새로운 행을 삽입하거나 삭제하여 두 번째 쿼리의 결과 집합이 첫 번째와 다른 경우를 말합니다. 이로 인해 한 트랜잭션 내에서 쿼리 결과의 일관성이 깨질 수 있습니다.

</div>
</details>

---

## 암호학/보안
<details>
<summary> 비대칭키 암호화, 대칭키 암호화에 대해 간단히 설명해주세요. </summary>
<div markdown="1">
대칭키 암호화는 암호화와 복호화에 같은 키를 사용하는 암호화 방식입니다.

비대칭키 암호화는 암호화와 복호화에 다른 키를 사용하는 암호화 방식입니다.

### 1. 대칭키(비밀키) 암호화

**장점**: 데이터를 암호화하기 위한 연산이 빨라 대용량 데이터 암호화에 적합, 구현이 용이, 기밀성을 제공
**단점**: 키를 교환해야하는 문제, 탈취 관리 걱정, 사람이 증가할 수록 키 관리가 어려움, 확장성 떨어짐

- 하나의 비밀키를 서버와 클라이언트 모두 함께 사용
- 암호화와 복호화에 같은 키를 사용하는 방식
- 비밀키 하나만 알아내면 암호화된 내용 해킹 가능
- 속도가 빠르다는 장점이 있지만, 키를 교환해야 한다는 문제가 있어서 중간에 탈취 당해 해킹당할 수 있다.
- (위험한 이유: 처음 상대방에게 대칭키를 전송하는 과정에서 탈취당하면 통신 내용 모두 해킹 가능)
- 서로 키를 보관해야 하기 때문에 관리해야 할 키가 방대해질 수 있다.

![대칭키(비밀키)](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FGTeWO%2Fbtsy2oZWZpu%2FTuxdc1d3GLkKjLF0shMa3K%2Fimg.png)

**대칭키(비밀키) 암호화의 종류**

- DES(Data Encryption Standard): 64-비트 블록 암호, 56-비트 비밀키 사용
- AES(Advanced Encryption Standard): 128-비트 블록 암호, 안전성 문제로 인해 DES 대체
- 아리아(ARIA): 한국에서 개발된 128-비트 블록 암호
- 시드(SEED): 한국에서 개발된 128-비트 블록 암호

### 2. 비대칭키(공개키) 암호화

**장점**: 키 분배 및 키 관리 용이, 기밀성/인증/부인 방지 기능 제공
**단점**: 속도가 느림, 상대적으로 키의 길이가 길다
  </div>
</details>

---

## 프로그래밍 패러다임
<details>
<summary> 객체지향과 절차지향에 대해 설명해주세요. </summary>
<div markdown="1">
  
## 절차지향 => 객체지향으로 바뀌는 이유

**절차지향 프로그래밍** 이란 물이 위에서 아래로 흐르는 것처럼 순차적인 처리가 중요시 되며, 프로그램 전체가 유기적으로 연결되도록 만드는 프로그래밍 기법으로 대표적인 절차지향 언어는 C언어가 있습니다.
장점은 컴퓨터의 처리구조와 유사해 실행속도가 빠르지만,단점으로 유지보수가 어렵고, 실행 순서가 정해져 있으므로 코드 순서가 바뀌면 동일한 결과를 보장하기 어려우며, 디버깅하기도 어렵습니다.
<br>
하지만 하드웨어의 발전으로, 성능에 조금 부담을 주더라도 큰 단점이 아니게 되었기에 모듈화, 캡슐화해서 개념적으로 접근하는 형태를 갖는 객체지향 프로그래밍이 탄생했습니다.
<br>
**객체 지향 프로그래밍(Object-Oriented Programming, OOP)** 은 프로그램을 객체라는 독립된 단위들의 모임으로 보고 개발하는 것입니다. 객체는 상태와 행위를 가지며, 
서로 메시지를 주고받고 데이터를 처리할 수 있습니다. 이러한 객체들이 서로 상호작용하면서 프로그램을 구성하는 것이 객체 지향 프로그래밍의 핵심입니다
<br>

## 절차지향 프로그래밍 (Procedural Programming)

절차지향 프로그래밍은 프로그램을 물 흐르듯 순차적으로 처리하는 방식으로, 대표적인 절차지향 언어는 C언어입니다.

**장점**:
- 컴퓨터의 처리구조와 유사하여 실행속도가 빠르다.
- 하드웨어의 발전으로 인해 성능 부담이 줄었다.

**단점**:
- 유지보수가 어렵다.
- 실행 순서가 고정되어 코드 순서 변경 시 동일한 결과를 보장하기 어렵다.
- 디버깅이 어렵다.

## 객체지향 프로그래밍 (Object-Oriented Programming, OOP)

객체지향 프로그래밍은 프로그램을 객체라는 독립된 단위들의 모임으로 보고 개발하는 방식입니다. 객체는 상태와 행동을 가지며, 서로 메시지를 주고받고 데이터를 처리할 수 있습니다.

### 객체지향 프로그래밍의 주요 특징:

1. **추상화 (Abstraction)**: 필요한 정보 중심으로 간소화된 모델을 제공합니다.

2. **캡슐화 (Encapsulation)**: 데이터와 기능을 하나로 묶어서 외부에 드러나지 않도록 합니다.

3. **상속성 (Inheritance)**: 클래스가 가진 데이터와 기능을 다른 클래스에 물려줍니다.

4. **다형성 (Polymorphism)**: 하나의 클래스나 메서드가 다양한 방식으로 동작할 수 있도록 합니다.

**장점**:
- 코드 재사용 및 확장 용이.
- 복잡한 프로그램을 객체 단위로 모델링하므로 유지보수가 쉽다.
- 캡슐화로 보안성이 높다.

**단점**:
- 실행 속도가 상대적으로 느리다.
- 메모리 사용량이 많을 수 있다.

### 절차지향 vs. 객체지향:

| 특성        | 절차지향              | 객체지향                |
|-------------|------------------------|--------------------------|
| 접근 방식   | Top-Down               | Bottom-Up                |
| 구성 요소   | 함수                   | 객체                     |
| 접근 제어   | 없음                   | public, protected, private |
| 다형성     | 불가능                | 함수, 생성자, 연산자 등 오버로딩 가능 |
| 상속        | 불가능                | 가능                     |
| 보안성     | 낮음                   | 높음                     |
| 데이터 공유 | 모든 함수 공유          | 객체 간 멤버 함수로만 공유 |

## 요약 및 참고 이미지

- 절차지향은 데이터 중심, 객체지향은 기능 중심입니다.
- 객체지향은 상속, 캡슐화, 다형성을 활용해 코드를 재사용하거나 확장하기 좋습니다.

![절차지향 vs 객체지향)](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcUDYl5%2Fbtsy9hU9Ce4%2FRRTEKUeF9IrR5xUJ7S1Wi1%2Fimg.png)
![절차지향 vs 객체지향)](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F2WX4V%2Fbtsy9gIOy1j%2Fxqm4a2LvgwOFxPT4j5XYlK%2Fimg.png)

</div>
</details>

<details>
<summary> 동기와 비동기 코드 실행방식에 대해 설명해주세요. </summary>
  <div markdown="1">

![동기 vs 비동기](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbUe0qA%2FbtszjDWMFQo%2FS1sHuCz8yhoUkYKlIaek41%2Fimg.png)

**동기(Synchronous)** 와 **비동기(Asynchronous)**
- **동기**는 요청을 보낸 후 응답을 받아야지만 다음 동작이 이루어지는 방식이다. 어떠한 태스크를 처리할 동안 나머지 태스크는 대기한다. 실제로 cpu가 느려지는 것은 아니지만 시스템의 전체 효율이 저하된다고 할 수 있다.

![동기식 처리모델](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FclMBVS%2Fbtszi7KCodC%2FNqfGUderS41KWxaG9CSUA0%2Fimg.png)

```
function func1(){
	console.log('1');
  func2();
}
function func2(){
	console.log('2');
  func3();
}
function func3(){
	console.log('3');
}

func1();
//결과 1,2,3
```

- **비동기** 는 요청을 보낸 후 응답의 수락 여부와는 상관없이 다음 태스크가 동작하는 방식이다. 자원을 효율적으로 사용할 수 있다. 이때, 비동기 요청시 응답 후 처리할 **Callback 함수** 를 함께 알려준다. 하지만 비동기 처리를 위해 여러 콜백함수를 중첩시키면 **콜백지옥** 이 발생한다. 이를 해결하기 위해 **Promise** 를 도입하였고, **Async / Await**  추가로 도입되었다. (Async / Await는  JavaScript에서 비동기 처리를 동기적인 방식으로 작성하게 해주는 문법)

![비동기식 처리모델](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FdZAmIj%2FbtszhvrtLF3%2FaBMUHmCpZjd0WmWdvxlkYk%2Fimg.png)

```
function func1() { 
  setTimeout(function(){
  console.log('1');
  }, 1000);
  func2(); 
} 
function func2() { 
  setTimeout(function() {
    console.log('2');
  }, 500); 
  func3(); 
} 
function func3() { 
  setTimeout(function(){
    console.log('3');
  }, 1500);
}

func1();

//결과 2, 1, 3
```

**동기가 사용되는 예시**
- 파일 시스템에서 파일을 읽는 작업: 파일을 읽은 후 해당 내용으로 작업하는 경우
- 데이터베이스에서 데이터를 읽어오는 작업 : DB에서 데이터를 읽은 후, 그 데이터를 다음 작업을 수행해야 하는 경우 동기처리가 필요함 (반대로 데이터 추출 작업이 빈번한 경우, 비동기식으로 하기도 함)

```
async createCollection(userId: number, name: string) {
try {
  const newBookmark = await this.collectionRepository.insert({
    user_id: userId,
  });
}
```

**비동기가 사용되는 예시**
- 웹 API 호출 : API를 호출하고 기다리는 동안 다른 작업도 수행
- setTimeOut 함수 : 주어진 시간이 지난후 특정함수가 실행되는 함수로 함수가 실행되는동안 다른 작업도 수행

**블로킹과 논블로킹**
- 흐름의 차단 여부를 결정

**블로킹**
- 제어권을 넘겨줌 - 명령이 수행되기 시작하면 프로그램 흐름의 제어권이 명령 수행중인 함수로 넘어감
**논블로킹**
- 제어권을 넘겨주지 않음 - 명령을 시키고 제어권은 여전히 메인이 가지고 있음

![동기비동기 블로킹논블로](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fdt2nzc%2Fbtszhn1l2NQ%2F2mrpkKgUHf4gQm6HycWnBK%2Fimg.png)

- Sync_Block : 위에서 설명한 동기방식과 동일
- Async_Non-Block : 위에서 설명한 비동기방식와 동일
- ***Sync_Non-block : 제어권을 메인에서 가지고 있어 다른일을 수행할 수 있지만 FuncA가 완료되어야만 다음 작업이 가능할때 사용 ex) 게임 로딩, 프로그래스바 - 둘다 제어권은 메인에서 가지고 있으며 로딩바의 작동은 지속적으로 보여지지만 데이터는 계속 로딩되고 있으며 로딩하고 있는 시스템에 계속해서 어느정도 로드 됬는지 조회한 후 로딩이 끝나야 다음 작업으로 넘어간다.***
- Async_Block : 실수나 잘못 구현한 경우가 아닌 경우 sync_block과 차이가 없기에 거의 사용되지 않음. node.js와 MYSQL의 경우 node.js에서 비동기 방식의 쿼리를 보냈을떄 MySQL에서 블로킹을 하기때문에 결국엔 동기처리와 다르지 않게 된다고 한다.
  </div>
</details>


