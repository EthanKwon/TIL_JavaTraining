# Oracle VirtualBox 5.2.26 , Ubuntu 18.04 설치 (19.02.12 기준) 

  **※학원에서 배운 내용을 그대로 복습하는 방식으로 만들었습니다. (사용 OS : Windows 7)**
  
 1. Oracle VirtualBox 5.2.26 설치 **(최신 버전 X)**
 
    * Oracle VirtualBox 다운로드 사이트 : [Oracle VirtualBox 5.2.26 다운로드](https://www.virtualbox.org/wiki/Download_Old_Builds_5_2)
    
    -> **Windows hosts**로 다운로드

 2. BIOS setting 하기 
 
      1) 컴퓨터 재부팅 후 **BIOS setting**으로 들어간다. (PC마다 F2나 DEL키로 들어갈 수 있다.)
    
      2) CPU에서 **Virtualrization**에서 **Enable** 선택
    
      3) **Save and reboot**를 한다.
    
 3. VirtualBox로 Linux 설치 
 
      1) 설치 전, **Ubuntu 18.04 64bit iso** 파일을 다운로드 한다. 
        
           * Ubuntu 18.04 64bit iso 파일 다운로드 사이트 : [Ubuntu 18.04 64bit 다운로드](https://www.ubuntu.com/download/desktop)
 
      2) 설치 과정중 다음의 설정들을 변경해준다. (배운내용을 기반으로 설정했기 때문에 "기본설정이 아닌것"을 참고해주세요.)
          
              Memory -> 2GB (2048MB)
              
              고정크기 설정
              
              저장위치 -> D드라이브
              
              하드용량 -> 30GB
          
          
      3) 설치 후, 설정에서 다음의 설정들을 변경해준다.
    
             일반 - 고급 - 클립보드 공유 -> 양방향 / 드래그 앤 드롭 -> 양방향
             
             시스템 - 프로세서 - 프로세서개수 -> 2개 / 실행제한 -> 90%
             
             저장소 - 컨트롤러 IDE -> 광학 드라이브 추가 -> Ubuntu 18.04 64bit iso파일 선택 
          
          
      4) 설정 완료 후, **"떼어 낼 수 있도록 시작"** 버튼을 실행해 **Ubuntu 18.04**를 설치한다. (일반 실행을 누르면 간혹 오류가 발생할 수 있습니다.)
          
          
  
