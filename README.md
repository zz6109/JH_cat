# 아두이노 리눅스 연결 문제 해결
## brltty : CH341을 연결 드라이버로 쓰게끔 강제함
## which brltty : 위치 찾은 다음에 삭제해야함
## 새 드라이버 CH34x를 설치해야함, 우선 업데이트 먼저 해줄것
## sudo apt-get update
## sudo apt-get upgrade
## https://github.com/juliagoda/CH341SER
## 위 링크에서 CH34x-master.zip 드라이버 설치 파일을 다운 받을것
## 해당 zip파일을 unzip으로 풀어주고 make 해주어야함
## 해당 makefile은 gcc-12 컴파일러를 사용한다. 
## sudo apt install gcc-12
## make
## sudo make load
## sudo rmmod ch341 : 기존 CH341 드라이버를 제거
## lsmod | grep ch34 : 기존 CH341 드라이버가 제거가 되었는지 확인
## 다시 pc와 아두이노를 연결 해주면 된다.

