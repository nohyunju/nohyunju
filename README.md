# 오픈소스sw개론 [과제2] README 파일 작성하기 20243158노윤주
**- top**

 현재 상태를 실시간으로 모니터링하는 명령어
 
 주로 시스템 관리자나 개발자들이 시스템의 성능 및 자원 사용량을 확인하기 위해 사용함
 
 top을 실행하면 CPU, 메모리, 스왑, 프로세스 등의 정보를 제공하며, 이 정보들은 주기적으로 업데이트되어 시스템의 현재 상태를 실시간으로 보여줌

 - q: top 명령어를 종료

 - h: 도움말을 표시

 - k: 특정 PID를 종료

 - r: 특정 PID의 우선순위를 변경

 - P: CPU 사용량 기준으로 정렬

 - M: 메모리 사용량 기준으로 정렬

 - T: 실행 시간 기준으로 정렬

![image](https://github.com/nohyunju/nohyunju/assets/166669186/93db1074-2bac-4dca-b60d-942ffbb31a32)

  
**- ps**
  
ps 명령어는 현재 실행 중인 프로세스를 보여주는 명령어

"Process Status"의 약어로, 시스템에서 실행 중인 프로세스에 대한 정보를 표시함

ps 명령어는 다양한 옵션을 사용하여 다양한 형식으로 정보를 표시할 수 있음.

  - -e: 시스템에 있는 모든 프로세스를 표시

  - -f: 전체 형식으로 출력하며, 프로세스의 상세 정보를 표시
    
  - -u <사용자명>: 특정 사용자의 프로세스만 표시
    
  - -p <프로세스ID>: 특정 프로세스 ID에 해당하는 프로세스 정보만 표시
    
예를 들어, ps -ef 명령어를 사용하면 시스템에 있는 모든 프로세스의 상세 정보를 표시함

![image](https://github.com/nohyunju/nohyunju/assets/166669186/ef873299-44ba-4670-a886-f5614d553abc)


  
**- jobs**

  쉘(shell)에서 현재 백그라운드(background)에서 실행 중인 작업을 나열하는 명령어
  
  백그라운드에서 실행 중인 작업 : 쉘에서 실행한 프로세스 중에서 백그라운드로 보내진 프로세스를 의미함

`jobs` 명령어를 실행하면 백그라운드에서 실행 중인 작업에 대한 목록이 표시됨

작업에는 작업 번호(job number)와 해당 작업이 실행되고 있는 상태 등의 정보가 포함됨

일반적으로 `jobs` 명령어는 쉘에서 백그라운드에서 실행 중인 작업을 확인할 때 유용하게 사용됨

- -l: 자세한 정보를 표시. 작업 번호, 상태, 실행 시간 등을 포함

- -n: 숫자로만 작업 번호를 표시

- -p: 작업의 프로세스 그룹 ID를 표시

- -r: 백그라운드에서 실행 중인 작업을 제외하고 모든 작업을 표시

- -s: 중단된 작업을 표시

**- kill**

리눅스나 유닉스 기반 시스템에서 프로세스를 종료하는 데 사용됨

특정 프로세스나 작업을 식별하고 그 작업에 시그널(signal)을 보내어 프로세스를 종료시킴

1. 특정 프로세스 종료
  
   `kill` 명령어를 사용하여 특정 프로세스를 종료시킴. 

   일반적으로는 프로세스의 PID(프로세스 ID)를 사용하여 프로세스를 식별하고 종료함 

   ex) `kill 1234`와 같이 입력하면 PID가 1234인 프로세스를 종료함

2. 시그널 전송
 
  `kill` 명령어를 사용하여 특정 시그널을 프로세스에 보낼 수 있음

   기본적으로 `kill` 명령어는 SIGTERM 시그널을 보내어 프로세스를 종료시킴. 하지만 다른 시그널을 사용하려면 `-<시그널>` 옵션을 사용할 수 있음

   ex) `kill -9 1234`와 같이 입력하면 PID가 1234인 프로세스에 SIGKILL 시그널을 보내어 강제로 종료함

3. 작업 종료
  
  `kill` 명령어를 사용하여 백그라운드에서 실행 중인 작업을 종료함
  
  `kill %작업번호`와 같이 작업 번호를 사용하여 해당 작업을 종료함

* `kill` 명령어를 사용할 때 유의해야 할 점은 권한이 있는 프로세스만 종료할 수 있음. 일반적으로 사용자는 자신이 소유한 프로세스나 관리자 권한을 가진 경우 다른 사용자의 프로세스를 종료할 수 있음.

