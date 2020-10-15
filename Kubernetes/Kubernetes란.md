# Kubernetes
----------------

## Introduction [2020.10.15]

> 컨데이너 가상화기술[docker]은 서비스간 자원격리를 하는데 별도의 OS설치 필요X
> -> OS 기동시간X
> -> 자동화시 빠르고 자원 효율 UP 
> -> 많은 서비스를 운형할때 일일이 배포 및 운영하는 역할x
> -> 컨테이너 오케스트레이터[여러 컨테이너를 관리하는 솔루션] 필요성 대두(Ex :Kubernetes)

> 운영자 : kubernetes의 cluster를 운영
> 사용자 : kubernetes의 기능들을 활용하여 자신의 서비스를 배포

----------------
## [기초편]: 쿠버네티스 설치

### h3 1.Why Kubernetes?
> Auto Scaling : 각 서버의 트레픽 평균을 가지고 서버의 개수 선정
> Auto Healing : 서버의 오류가 발생했을 때 여분의 서버 1개로 이관하여 서비스 지속
> Deployment   : 업데이트 자동화

> 운영효율이 높아지고 -> 서버의 개수가 줄어들고 -> 운영비용이 감소하고

### h3 2.VM vs Container
VM : 각각의 OS를 띄움
> Host Server ->Host OS ->Hypervisor(vm) -> Guest OS

Container : 하나의 OS공유
> Host Server-> Host OS ->Software verturalize service -> Container

OS에서 제공되는 자원격리 기술사용 -> Container 단위로 분리
> namespace : 커널 관련 영역 분리
> cgroups   : 자원 관련 영역 분리


----------------
## [기초편]: 기본 오브젝트

----------------
## [기초편]: 컨트롤러

----------------
## [중급편]: Pod

----------------
## [중급편]: 기본 오브젝트

----------------
## [중급편]: 컨트롤러

----------------
## [CKA편]: 개요 및 시험 공부

----------------
## [아키텍쳐편]