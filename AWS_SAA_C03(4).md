# AWS SAA C03 / Network

# Route53

![Route53](./pictures/Route53.png)

AWS에서 제공하는 DNS(Domain Name System) 서비스.

- Authoritative DNS 서비스이다. (내가 직접 DNS 레코드를 업데이트 할 수 있음)

## Record Type

- A: hostname을 IPv4에 매핑 한다.

- AAAA: hostname을 IPv6에 매핑 한다.

- CNAME: hostname을 다른 hostname에 매핑 한다.

- NS: 도메인에 대한 트래픽이 어떻게 라우팅될지를 제어하는 서버의 집합이다.

- CNAME vs Alias:

  - CNAME: NON-ROOT domain에만 사용 가능. EC2에 사용 가능.

  - Alias: ROOT domain에도 사용 가능. 무료. native health check 제공. EC2는 Alias를 설정할 수 없다.

## Hosted Zone

Public Hosted Zone: 인터넷에서의 트래픽에 응답할 수 있다.

Private Hosted Zone: 하나 혹은 그 이상의 VPCs에서 온 요청에 응답할 수 있다.

# CloudFront

![CloudFront](./pictures/CloudFront.png)

AWS의 Content Delivery Network(CDN) 서비스이다.

- 약 216개의 Edge Location이 있으며 컨텐츠가 Edge에서 캐싱된다.

- 컨텐츠가 세계적으로 분산되어 있기 때문에 DDoS에서 보호된다.

- Shield, AWS Application Firewall과 통합할 수 있다.

# Global Accelerator

![Global_Accelerator](./pictures/Global_Accelerator.png)

전 세계에 분산된 AWS 엣지 위치를 활용하여 사용자의 트래픽을 최적의 경로로 안내하는 서비스.

- UDP 및 TCP 지원.

- Unicast 기반.

- 게임, IoT, 음성 통신과 같은 비 HTTP 기반 어플리케이션에 특히 유용.

- AWS 리소스에 대해 고정된 정적 IP 주소를 제공한다.

## CloudFront vs Global Accelerator

공통점:

- 글로벌 네트워크와 엣지 로케이션을 사용한다.

- DDoS 보호를 위해 AWS Shield와 통합된다.

차이점:

- CloudFront는 캐싱 기능 사용. Global Accelerator는 캐싱을 사용하지 않는다.

# API Gateway

![API_Gateway](./pictures/API_Gateway.png)

AWS의 서버리스 서비스로, REST API를 생성할 수 있다.

- 단순히 HTTP 앤드포인트가 아니라 인증, 사용량 계획, 개발 단계 등의 기능을 제공한다.

- Lambda와 조합하면 인프라가 필요 없는 Serverless 어플리케이션을 구축할 수 있다.

- API 버전 핸들링이 가능하다.

- dev, test, prod 등의 환경을 핸들링 가능하다.

- 보안 관련 핸들링이 가능하다.

- 요청을 쓰로틀링 하는 것이 가능하다.

- Swagger나 Open API를 통해 정의서를 가져오거나 내보낼 수 있다.

- 요청과 응답을 가공할 수 있다.

- API 응답을 캐싱이 가능하다.

- 어떠한 AWS 서비스도 노출시켜 직접 접근하도록 할 수 있다.

## Endpoint Types

### Edge-Optimized (default)

- 글로벌 클라이언트를 위한 서비스

- CloudFront Edge locations를 통해 요청이 가능하다.

- API Gateway는 여전히 한 지역에 존재한다.

### Regional

- 같은 지역에 있는 클라이언트를 위한 서비스.

- 수동으로 CloudFront와 연동할 수 있다.

### Private

- VPC 내부에서만 접근이 가능하고, intergace VPC endpoint (ENI)를 사용한다.

- 접근을 정의하기 위해 resource policy를 사용한다.
