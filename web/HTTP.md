# HTTP

## HTTP란?

- HyperText Transfer Protocol
- www 상에서 하이퍼텍스트 문서를 전송하기 위해 사용되는 통신규약

## HTTP의 역사

- 1991년: HTTP 0.9 발표
- 1996년: HTTP 1.0 발표
- 1999년: HTTP 1.1 발표
- 2009년: SPDY 1.0 발표 (후에 HTTP/2의 기반이 됨)
- 2012년: SPDY 2.0 발표
- 2015년: HTTP/2 발표

## HTTP/0.9

- HTTP의 가장 초기 버전이다.
- 확장성을 염두에 두고 발표하였다.
- 참고문서: [https://www.w3.org/Protocols/HTTP/AsImplemented.html](https://www.w3.org/Protocols/HTTP/AsImplemented.html)

### 주요 특징

- GET method와 파일 경로만을 이용한 요청 방식
- 헤더 구조 없음
- 다른 문서형식은 전송불가
- 상태코드, 에러코드, url, 헤더코드가 없음
- Hypertext만 응답 가능
    - 헤더코드가 없어 다른 형태의 문서는 보낼 수가 없었음
    - (Hyptertext를 위한 프로토콜로 시작했기 때문에 초창기 모델로는 당연하다고 생각)

### 예시

(추가 예정)

## HTTP/1.0

### 주요 특징

- 헤더 영역 추가
    - HTTP 버전, 상태 코드, content type 표시
- Methods: GET, HEAD, POST
- 헤더에 'Content-Type'이 추가되어 하이퍼텍스트 외 다른 형식의 파일도 응답 가능

### 예시

(추가 예정)

## HTTP/1.1

- 가장 보편적으로 쓰이고 있는, 쓰였던 첫 표준화된 버전
- 네트워크 통신과 관련하여 1.0에서 문제가 있었던 부분을 최적화하고 보완하였다.
- 헤더 강화
    - timeout을 추가하여 연결이 끊기지 않도록 했다.

## HTTP/2.0

### 등장 배경

- 1.1 버전의 통신 방식으로 인해 발생하는 속도를 해결하고자 등장
- 구글에서 속도를 개선한 프로토콜을 SPDY라는 이름으로 제안했고, 이를 기반으로 HTTP/2.0로 표준화된 프로토콜이 만들어졌다.

### 달라진 점

- TLS 위에서만 동작
- 서버 푸시
    - 클라이언트의 요청이 없이도 서버에서 강제 푸시가 가능하다.
    - 클라이언트의 요청 latency가 제거되어 속도를 증가시킬 수 있다.
- HTTP 헤더 압축
    - 1.1에서는 헤더 정보가 같더라도 매번 중복된 정보로 헤더 정보를 보내야 했음
    - 중복되는 정보는 굳이 처리하지 않고 다른 정보만 뽑아내는 작업을 통해 헤더를 압축한다.
- 바이너리로 프레임을 구성

## 참고 문서

- [https://medium.com/platform-engineer/evolution-of-http-69cfe6531ba0](https://medium.com/platform-engineer/evolution-of-http-69cfe6531ba0)