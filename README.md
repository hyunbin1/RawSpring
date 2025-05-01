# RawSpring

## 직접 구현해야 할 Spring 핵심 기능 정리
1. 서블릿 컨테이너
ServerSocket → 요청 수신

요청 파싱 + 응답 직렬화

URL 라우팅 및 매핑 시스템

2. Dispatcher 구조
프론트 컨트롤러

URL, HTTP Method 기반으로 컨트롤러 메서드 호출

리턴 값 → 응답 포맷으로 변환

3. 어노테이션 기반 DI 시스템
@MyController, @MyService, @MyAutowired

리플렉션 기반 클래스 스캔 + 의존성 주입

4. 멀티스레드 처리
ExecutorService, ThreadPoolExecutor

요청별 Thread-safe 설계 (RequestContext 같은 구조도 직접)

5. Bean Lifecycle 관리
초기화, 소멸 훅

싱글톤 관리, 프로토타입 스코프 등도 가능

6. 예외 처리기
@MyExceptionHandler 클래스 자동 탐지 및 호출

7. 직렬화 & 응답 변환
객체 → JSON 변환 (Jackson 없이 직접)

@MyResponseBody 처리기
