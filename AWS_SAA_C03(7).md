# AWS_SAA_C03(7) / Monitoring & Architect

# Step Functions

![Step_Functions](./pictures/Step_Functions.png)

워크플로우를 시각적으로 구성할 수 있는 서버리스 형태의 기능. 주로 람다 함수를 오케스트레이션 하는 데 활용한다.

- EC2, ECS, On-premises, API Gateway, SQS 등과 연동할 수 있다.

# CloudWatch

![CloudWatch](./pictures/CloudWatch.png)

AWS의 모든 서비스에 대한 지표를 제공하는 서비스.

- CPUUtilization, NetworkIn등을 모니터링 할 수 있다.

- 측정 항목에는 타임스탬프가 있다.

- 지표의 CloudWatch 대시보드를 생성할 수 있다.

- 대시보드 공유 기능을 통해 계정을 생성하지 않고 유저가 대시보드에 접근할 수 있다 (이후 유저 고유의 비밀번호 생성)

# EventBridge

![EventBridge](./pictures/EventBridge.png)

AWS의 다양한 이벤트에 대한 처리를 구성하는 서비스.

# CloudTrail

![CloudTrail](./pictures/CloudTrail.png)

AWS 계정에 대한 governance, compliance, audit기능을 제공한다.

- AWS계정 내의 Console, SDK, CLI, AWS Services에 의한 이벤트, API콜 기록을 가져온다.

- 모든 리전 또는 단일 리전에 적용 가능하다.

# Config

![Config](./pictures/Config.png)

AWS 리소스의 규정 준수를 감사하고 기록하는 서비스.

- 보안 그룹 내의 SSH 액세스가 가능한지, 변경사항에 대한 알림이 가는지 등을 감사할 수 있다.

- 구체적인 구성 관리, 변경 추적, 규칙 위반 구성 변경 감지.

# Trusted Advisor

![Trusted_Advisor](./pictures/Trusted_Advisor.png)

AWS 환경의 최적화를 돕는 서비스.

- 다양한 체크 및 필요에 다른 이메일 알림 설정.

- 광범위한 Best Practice 제시.
