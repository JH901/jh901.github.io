# Docker
-----------------------
### 도커를 왜 쓸까?
 - Debug your app, not your environment
 - Securely build and share any application, anywhere
 
### 도커의 역사 & 현위치
 - 클라운드 환경에서의 표준

### 도커 설치
Windows : 도커 영접할 준비

    - Windows 10 프로, 엔터프라이즈, 교육용
    https://docs.docker.com/docker-for-windows/install/
    - Windows 10 Home
    https://docs.docker.com/toolbox/toolbox_install_windows/
    
    Install Docker toolbox >> download (.exe) file  >> execute file
    
    next > next > next > next > finish
    
    select 'Docker quick start terminal'
    
    docker --version

Mac : 도커 영접할 준비

    https://docs.docker.com/docker-for-mac/install/
    
    Download from Docker Hub > Create account > Download Docker Desktop for Mac
    
    drag and drop Docker icon to Applications folder 
    
    search docker > open > click docker icon
    
    terminal : docker --version
    
Ubuntu : 도커 영접할 준비
    - terminal
    curl -fsSL https://get.docker.com -o get-docker.sh
    sudo sh get-docker.sh
    sudo usermod -aG docker {Ubuntu user name}
    
    