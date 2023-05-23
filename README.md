# FRi_230517


## top
### top의 역할

- CPU와 메모리 이용에 관한 정보를 표시
- 옵션 없이 입력시 3초 간격으로 화면을 갱신

### top의 옵션

- shitf + p : CPU 사용량이 큰 순으로 정렬
- shift + m : 메모리 사용량이 큰 순으로 정렬
- shitf + t : 실행된 시간이 큰 순으로 정렬 
- k : 프로세스 종료
- c : 명령인자 표시/비표시
- u : 입력한 유저소유의 프로세스만 표시
- q : 명령어 종료
- h : 
### top의 사용

![image](https://user-images.githubusercontent.com/85490910/240101268-fbd6ab5e-4fd0-4b25-bf8c-894f44a6ff62.png)
>top의 실행 화면

![image](https://user-images.githubusercontent.com/85490910/240101269-0d4a3e88-d799-4b7c-83a6-cc5859cc65cc.png)
>23:57:41 : 현재시간
>
>6 min : uptime
>
>0 users : 현재 접속된 사용자
>
>load average : CPU의 부하율 좌측 부터 1분, 5분, 15분 평균을 측정 

![image](https://user-images.githubusercontent.com/85490910/240101264-d695143b-d76c-41c0-9b05-4d9e48379b1b.png)
>Tasks : 총 4개의 프로세스가 가동중
>
>running : 1개의 프로세스가 작동중
>
>sleeping : 3개의 프로세스가 대기중
>
>stopped : 0개의 프로세스가 멈춘 상태
>
>zombie :  0개의 프로세스가 좀비 상태

>%Cpu(s) 
>>0.4 us : user level 에서 사용하고 있는 cpu 비중 
>>
>>3.0 sy : system level 에서 사용하고 있는 cpu 비중 커널에서 사용되는 시간 wa, id, hi, si 제외
>>
>>0.0 ni : 기본값보다 낮은 우선순위로 user level 에서 실행된 시간
>>
>>96.5 : id idle 상태의 cpu 비중 
>>
>>0.0 wa : system 이 io 요청을 처리하지 못한 상태의 cpu 비중
>>
>>0.2 hi :핸들러에서 사용한 시간
>>
>>0.0 si :  잠시 미뤄둔 interrupt 처리 작업에 사용한 시간
>>
>>0.0 st : 가상 CPU 가 실제 CPU 를 기다리는 시간을 백분율로 표시

>KiB Mem

>>8340816 total : 전체 물리적인 메모리
>>
>>4997820 free : 사용되지 않는 여유 메모리
>>
>>3113644 used : 사용중인 메모리
>>
>>229352 buff/cache : 버퍼된 메모리

>KiB Swap

>>25165824 total : 전체 스왑 메모리
>>
>>25065972 free : 남아있는 스왑 메모리
>>
>>99852 used : 사용중인 스왑 메모리
>>
>>5093440 avail Mem : 새로운 애플리케이션을 시작 할 수 있는 메모리 양을 추정 

![img](https://user-images.githubusercontent.com/85490910/240103876-1b173c2e-6532-4cc5-aebc-8fc3a51aaeb9.png)

>PID : 프로세스 ID
>
>USER : 프로세스를 사용하는 사용자
>
>PR : 프로세스 우선순위
>
>NI : NICE 값, 낮을 수록 우선순위가 높음
>
>VIRT : 가상메모리 사용량 
>
>S : 프로세스 상태 [ S, R, W, Z ]
>
>%CPU : CPU의 사용률
>
>%MEM : 메모리 사용률
>
>COMMAND : 실행된 명령어

## ps

### ps의 역할

- 현재 실행되고 있는 프로세스 표시

### ps의 옵션

- -A : 모든 프로세스 출력
- a : 터미널의 사용자 고유 프로세스 출력
- -a : 세션리더 및 터미널과 관련되지 않은 프로세스를 제외한 모든 프로세스 출력
- -e : 커널 프로세스를 제외한 모든 프로세스 출력
- -f : 풀 포맷으로 보여줌
- -l : 롱 풀포맷으로 보여줌
- r : 현재 실행중인 프로세스 출력
- -x : 터미널 없는 프로세스 출력
- -d : 세션 리더를 제외한 모든 프로세스 출력

### ps의 사용

>ps의 실행화면

![png](https://user-images.githubusercontent.com/85490910/240109262-5b983948-d830-4920-935d-958b2ab882b5.PNG)

>ps -elf의 실행화면

![png](https://user-images.githubusercontent.com/85490910/240109256-e8b4f8ae-3d52-4c59-8242-e583a7198750.PNG)

>UID : 프로세스 소유자의; 이름
>
>PID : 프로세스 식별 번호
>
>PPID : 부모 프로세스 ID
>
>%CPU : CPU사용 비율의 추정치
>
>%MEM : 메모리 사용 비율 추정치
>
>VSZ : k단위 또는 페이지 단위의 가상메모리 사용량
>
>RSS : 실제 메모리 사용량
>
>TTY : 프로세스와 연결된 터미널
>
>S,STAY : 현재 프로세스의 상태코드
>
>TIME : 총CPU 사용시간
>
>COMMAD : 현재 프로세스의 실행 명령어
>
>STIME : 프로세스가 시작된 날짜 혹은 시간
>
>C,CP : 짧은 기간 동안의 CPU 사용률
>
>F : 프로세스의 플래그
>
>PRI : 실제 실행 우선순위
>
>NI : nice 우선순위 번호

### ps와 top의 차이

**ps는 ps한 시점에서 proc에서 검색한 cpu사용량을 나타냄
**top는 그때그때의 cpu사용량을 나타냄

## jobs

### jobs의 역할

- 백그라운드에 실행되는 작업 목록(작업 번호,상태,명령어)을 보여줌
>작업 번호는 PID와 달리 별도로 부여되는 작업목록상의 번호임

### jobs의 옵션
- -p : 백그라운드에 있는 프로세스의 아이디(PID)만 출력
- -l : 백그라운드에 있는 프로세스 아이디(PID)를 함께 출력
- -s : 백그라운드에 있는 프로세스 중 멈춰있는 프로세스만 출력
- -r : 백그라운드에 있는 프로세스 중 실행중인 프로세스만 출력

### jobs의 사용







