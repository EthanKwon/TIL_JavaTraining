# file input output commend & process commend

**※학원에서 배운 내용을 그대로 복습하는 방식으로 만들었습니다. (사용 OS : Ubuntu 18.04)**


### 파일의 속성 확인 하는 방법

```
ex) - rw-r--r-- 1 root root 223 7월 2 2018 파일명
```

1. '-' : 파일의 종류  
2. (owner)(group)(others) : 파일 접근 권한 표시  
3. 1 : 하드링크 개수  
4. root : 파일 소유자의 로그인 ID  
5. root : 파일 소유자의 그룹이름  
6. 223 : 파일의 크기  
7. 7월 2 2018 : 마지막을 수정된 날짜  
8. 파일명 : 파일 명  


  * **file : 지정한 파일의 종류를 알려줌**

### 접근 권한의 종류

```
읽기(r) : 파일을 읽거나 복사 할 수 있다.

쓰기(w) : 파일을 수정/이동/삭제 할 수 있다.

실행(x) : 파일을 실행할 수 있다.
```

  * **chmod : 파일이나 디렉터리 접근 권한을 변경한다.**

```
owner(u) /  group(g) / others(o) / All user(a)

권한부여(+) / 권한취소(-)

읽기(r) / 쓰기(w) / 실행(x) 
```

**※숫자를 이용하는 방법 : rwx 를 8진수로 표현 (4/2/1)**

### 특수한 권한 부여하기 

```
* SetUID : 맨 앞자리가 4(owner의 x -> s)

-> 파일이 실행되는 동안 파일 소유자의 권한으로 실행


* 스티키 비트 : 맨 앞자리가 0(others의 x -> t)

-> 설정 시, 이 디렉터리에는 누구나 파일 생성 가능
```

  * **chown : 사용자 owner 변경하기 (root 사용자의 경우)**

------

### 유닉스에서 프로세스 생성하기

  #### 프로세스의 부모-자식 관계

```
parent process -> child process
```

  **※ 프로세스의 고유번호 : PID**  

  * **ps : 프로세스의 상태를 보여준다.**  

```
옵션 : -f(상세한 정보 출력), a(실행한 정보 출력)
```

### signal

* 지원하는 시그널의 목록은 kill - l 명령으로 알수 있다.

```
 kill [PID]: 지정한 시그널을 프로세스에 보낸다.  
 
-> 2: 인터럽트 시그널을 보낸다.
-> 9: 프로세스를 강제로 종료한다.
-> 15:프로세스와 관련된 파일을 정리한 후 종료한다. (단, 종료되지 않는 프로세스가 있을 수 있다.)
```

※ pkill 명령어를 통해서 명령 이름(CMD)으로 프로세스를 찾아 종료 할 수 있다.

* **top : 현재 실행 중인 프로세스에 대한 정보를 주기적으로 출력**

### 포그라운드 / 백그라운드 작업 제어  

```
포그라운드 / 백그라운드 : sleep 100 / sleep 100 &

fg : 작업 전환 하기

Ctrl + c : 작업 종료하기 
```

  * **jobs: 백그라운드 작업을 모두 보여준다.** 
  
### 작업 예약 

  * **at : 예약한 작업을 정해진 시간에 실행**


### 정해진 시간에 반복 실행

  * **crontab : 사용자의 crontab 파일을 관리**

