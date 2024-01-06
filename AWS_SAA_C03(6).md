# AWS_SAA_C03(6) / Container

## ECS

Elastic Container Service의 약자로 Docker 컨테이너를 간편하게 배포할 수 있는 AWS의 완전 관리형 서비스이다.

- ECS 클러스터에서 ECS 테스크를 실행하는 형태로 작동한다.

### ECS Cluster - EC2 Launch Type

- EC2 인스턴스 유형으로 ECS를 실행하면 EC2 인프라를 관리해야 한다.

- 각각의 EC2 인스턴스는 ECS Agent를 실행해야 한다.

### ECS Cluster - Fargate LaunchType

- EC2 인스턴스를 관리하지 않는 서버리스 서비스이다.

- ECS Task만 정의하면 필요한 CPU, RAM에 따라 자동으로 실행된다.

## ECR

Elastic Container Registry의 약자로 Docker 컨테이너 이미지를 저장, 관리, 배포하는 완전 관리형 서비스이다.

- S3를 기반으로 한다.

## EKS

Elastic Kubernetes Service의 약자로 AWS에서 제공하는 관리형 Kubernetes 클러스터 서비스이다.

- ECS와 유사하지만 다른 API를 사용한다. (오픈소스)
