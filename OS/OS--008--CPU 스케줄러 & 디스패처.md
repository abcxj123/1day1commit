### CPU Scheduler & Dispatcher
- CPU Scheduler는 Ready 상태의 프로세스 중에서 이번에 CPU를 줄 프로세스를 고른다.
- Dispatcher는 CPU의 제어권을 CPU Scheduler에 의해 선택된 프로세스에게 넘겨준다.
- 이 과정을 Context Switch(문맥 교환)라고 한다.
***
### CPU 스케줄링
CPU 스케줄링이 필요한 경우는 프로세스에게 다음과 같은 상태 변화가 있는 경우이다.  
1. Running -> Blocked (예 : I/O 요청하는 시스템 콜)  
2. Running -> Ready (예 : 할당 시간 만료로 Timer Interrupt)
3. Blocked -> Ready (예 : I/O 완료 후 Interrupt)
4. Terminate
- 1, 4번은 강제로 빼앗지 않고 자진해서 반납한다. (**nonpreemptive**)
- 2, 3번은 강제로 빼앗는다. (**preemptive**)
