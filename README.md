# FRi_230517


# Heading 2
## top의 역할

- CPU와 메모리 이용에 관한 정보를 표시
- 옵션 없이 입력시 3초 간격으로 화면을 갱신

## top의 옵션

- shitf + p : CPU 사용량이 큰 순으로 정렬
- shift + m : 메모리 사용량이 큰 순으로 정렬
- shitf + t : 실행된 시간이 큰 순으로 정렬 
- k : 프로세스 종료
- c : 명령인자 표시/비표시
- u : 입력한 유저소유의 프로세스만 표시
- q : 명령어 종료

## top의 사용

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

![imgage](https://user-images.githubusercontent.com/85490910/240101264-d695143b-d76c-41c0-9b05-4d9e48379b1b.png)
>Tasks : 총 4개의 프로세스가 가동중
>
>running : 1개의 프로세스가 작동중
>
>sleeping : 3개의 프로세스가 대기중
>
>stopped : 0개의 프로세스가 멈춘 상태
>
>zombie :  0개의 프로세스가 좀비 상태


