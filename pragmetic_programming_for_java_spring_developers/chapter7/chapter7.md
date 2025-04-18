# 서비스
도메인 객체나 도메인 서비스라고 불리는 도메인에 일을 위임하는 공간

## 역할
- 도메인 객체를 불러온다.
- 도메인 객체나 도메인 서비스에 일을 위임한다.
- 도메인 객체의 변경 사항을 저장한다.

## 도메인, 도메인 서비스, 애플리케이션 서비스
### 도메인
- 도메인 역할을 수행

### 도메인 서비스
- 도메인 객체에 기술할 수 없는 연산 로직을 처리

### 애플리케이션 서비스
- 도메인을 저장소에서 볼러옴
- 도메인 혹은 도메인 서비스를 실행

## 어떤 순서로 개발을 해야하는가?
**도메인 모델 > 도메인 서비스 > 애플리케이션 서비스**
- 코드의 의존성이 명확하게 드러나기 때문에 테스트 작성이 용이해짐

## 트랜잭션 서비스를 어떻게 개선할 수 있는가?
1. 해당 비즈니스 로직을 새로운 서비스에 위임
2. 해당 비즈니스 로직을 새로운 도메인에 위임

## 객체지향으로 보는 서비스
1. 서비스는 가능한 적게 만들고, 얇게 유지해야함
2. 서비스보다 풍부한 도메인을 만들어야함

## 서비스는 어떤 요건을 갖추어야하는가?
- 도메인의 연산을 처리하기 때문에 동일한 입력에 동일한 출력을 보장해야함
- 불변성이 보장되어야함

## 서비스를 서비스 답게 만드는 방법
- 서비스 멤버 변수는 final로 선언
- 세터는 존재하면 안됨
- 반드시 생성자 주입으로 객체를 주입 받아야함
- 비즈니스 로직은 서비스가 아닌 도메인에 있어야함
- 서비스를 얇게 유지해야함