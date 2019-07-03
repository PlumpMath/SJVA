##### <span style="color:red">■ 0.1.6.0 (2019-07-03)</span> #####
- 플러그인 : 토렌트 - 다운로드 국내TV 추가<br>

- 플러그인 : 토렌트 - 다운로드<br>
  목록 화면 추가
  
##### ■ 0.1.5.6 (2019-06-29) #####
- 플러그인 : 토렌트 - 다운로드 - 상태 추가<br>

- 시스템 - 설정<br>
  로그인 사용 on / off 추가<br><br>
  ![](https://cdn.discordapp.com/attachments/590833735197261874/594050242752675841/unknown.png)

##### ■ 0.1.5.3 (2019-06-28) #####
- 플러그인 : 토렌트 - RSS - 설정 - 스케쥴링<br>
  DB삭제 버튼 추가. 스케쥴 삭제시 DB도 삭제하도록 변경<br><br>
  ![](https://cdn.discordapp.com/attachments/590833735197261874/593987902309138434/unknown.png)

- 🐞: javnet 주소 변경.<br> <b><span class="text-danger">주소가 변경되면서 게시판을 새로 만들었기 때문에, 기존 DB를 삭제해 주어야 함.</span></b>

##### ■ 0.1.5.2 (2019-06-26) #####
- 플러그인 : 토렌트 - Offcloud<br>
  목록화면에서 다운로드 프로그램에 다운로드 요청할 수 있도록 버튼 추가

##### <span style="color:red">■ 0.1.5 (2019-06-26)</span> #####
- SMI to SRT 플러그인 추가<br>
  [(메뉴얼 : SMI to SRT (SJVA, Plex plugin, shell))](https://soju6jan.com/archives/510)

- 플러그인 : 파일처리 - 국내TV<br><br>
  회차 삭제 예외 장르 옵션 추가<br>
  파일처리시 Daum에서 검색은 되나 에피소드 정보가 없는 방송은 파일명에서 회차 정보를 없애고 있음.<br>애니메이션 등과 같은 장르는 회차 정보가 거의 없어서 항상 회차 정보를 없애는 문제가 있어 옵션 추가.<br>all 입력시 회차 정보를 제거하지 않음.<br><br>
  ![](https://cdn.discordapp.com/attachments/590833735197261874/593343517904994304/unknown.png)

- 플러그인 : 토렌트 - Offcloud<br><br>
  http링크 리모트 추가 옵션 추가<br>
  주로 자막을 같이 받는 용도<br><br>
  ![](https://cdn.discordapp.com/attachments/590833735197261874/593343034092158977/unknown.png)<br><br>
  ![](https://cdn.discordapp.com/attachments/590833735197261874/593342835659636736/unknown.png)

- 시스템 - 설정 로그 레벨 옵션 추가<br>
  안정화 되신 분들은 DEBUG 상위 옵션을 사용하여 속도 개선<br><br>
  ![](https://cdn.discordapp.com/attachments/590833735197261874/593416440225202187/unknown.png)

- 🐞: offcloud cache 확인 화면에서 hash로 다운로드 안 되는 문제 수정<br>

- 🐞: 텔레그램 RSS 수신 메시지중 다음 링크가 작동안하는 문제 수정<br>


##### ■ 0.1.4.9 (2019-06-25) #####
- 🐞: Trnasmission 다운로드 안 되는 문제 수정<br>

##### ■ 0.1.4.6 (2019-06-24) #####
- 🐞: Trnasmission 접속 URL 버그 수정<br>

- Plex SJVA 플러그인 업데이트<br>
  🐞: 윈도우 Plex 서버에서 '보좌관 – 세상을~~' 스캔 안되는 문제 대응.<br>
       특수문자로 인해 부분 스캔이 안되며 드라마 폴더를 스캔함.
  
- Plex 설정에 추가 스캔 Plex URL 옵션 추가.<br>
    - 이 기능은 주 Plex 서버 이외에 다른 Plex에서도 스캔 명령을 받고자 할 때 사용.<br>
![](https://cdn.discordapp.com/attachments/590833735197261874/592668631557472267/unknown.png)

    - 오른쪽 주 서버고 왼쪽 부 서버.<br>하나의 SJVA 로 여러 Plex에 스캔 명령 전달. 각 Plex의 라이브러리 구성에 따라 적절한 스캔 명령 수행<br>
스캔 요청 파일이 라이브러리에 없는 경우 무시
![](https://cdn.discordapp.com/attachments/590833735197261874/592668470559375380/unknown.png)

    - 부 Plex 서버 설정. 주 Plex 서버와 OS가 다르거나 마운트 경로가 다른 경우 경로 변경 규칙 설정<br>
![](https://cdn.discordapp.com/attachments/590833735197261874/592722478783004689/unknown.png)
    
    - 위 규칙에 의해 파일경로 변경하여 스캔. 오른쪽 주 서버(윈도우), 왼쪽 부 서버(Synology)<br>
![](https://cdn.discordapp.com/attachments/590833735197261874/592726516341932042/unknown.png)

- 툴 - DaumTV Refresh 버튼 추가 및 1일 다회차 방송 버그 수정<br>
  ※ "슬플 때 사랑한다" Daum 회차 정보를 보면 22(3.28) 21(3.30) 23(3.30) 순으로 나옴. 회차 정보가 잘못 되어 있고, 이로 인해 1일 1회로 인식하는 문제가 있어 반올림 방식으로 변경. 방송종료 + DB에 저장된 방송은 크롤링 하지 않고 DB에서 바로 읽어 사용하는 데 잘못된 정보가 있을 경우 수정할 방법이 없어 Refresh 버튼 추가.<br>
  ※ 1일 다회차 인식을 못했을 때 발생하는 현상. (상단 정상, 하단 1일 1회)
  ![](https://cdn.discordapp.com/attachments/590833735197261874/592548005987483671/unknown.png)

  

##### ■ 0.1.4.3 (2019-06-23) #####
- 토렌트 - 다운로드 추가 (개발중)<br>
  트랜스미션과, 다운로드스테이션 정보 입력 후 다운로드 메뉴나 타 플러그인 링크를 클릭하여 다운로드 추가 가능

- 티빙 다운로드모드 추가
  
- 푹, 티빙 화이트리스트 모드시 첫회 받기 옵션 추가
![](https://cdn.discordapp.com/attachments/590833735197261874/592028501092073503/unknown.png)    
    

- 🐞: 푹 화이트리스트 모드 일 경우 QVOD 받는 문제 수정<br>
- 🐞: RSS검색화면에서 Offcloud 버튼 동작 안되는 문제 수정

##### ■ 0.1.3.17 (2019-06-19) #####
- 시스템 - 설정 - 웹 설정에서 테마 기능 추가<br>
![](https://cdn.discordapp.com/attachments/590833735197261874/590975960250187852/unknown.png)


##### ■ 0.1.3.16 (2019-06-19) #####
- AV 파일명 변경시 원본파일명 유지 옵션 추가<br>
  ※ (XXX.com)ABC-123.mp4  => abc-123 [(XXX.com)ABC-123].mp4


##### ■ 0.1.3.15 (2019-06-19) #####
- 푹 다운로드 모드 선택 추가. <br>
  화이트리스트일 경우 포함 프로그램에 있는 방송만 다운로드<br><br>
![](https://cdn.discordapp.com/attachments/590833735197261874/590833908107575301/unknown.png)<br>
![](https://cdn.discordapp.com/attachments/590833735197261874/590835040259145738/unknown.png)

##### ■ 0.1.3.14 (2019-06-19) #####
- 시스템 - 정보 메뉴 추가<br>
- 🐞 : ffmpeg 배속이 안나오는 문제 수정


##### ■ 0.1.3.12 (2019-06-18) #####
- 텔레그램 봇 RSS 수신시 Daum URL 같이 전송 (파일명으로 검색되는 TV쇼만)

- /flaskfilemanager 로그인 없이 접속되는 문제 수정

- ffmpeg version 2.6.9 버전 다운로드 성공 <br>
  (Synology debian-chroot 의 기본 버전)<br>

- ffmpeg time regex 수정 : 일부 다운로드 되지 않는 영상 다운로드


##### ■ 0.1.3.8 (2019-06-18) #####
- 텔레그램 봇 단체방 변경으로 인한 수정<br>
 [(메뉴얼 : 텔레그램 봇 단체방 변경)](https://soju6jan.com/archives/493)


##### <span style="color:red">■ 0.1.3 (2019-06-14)</span> #####
- AV 관련 업데이트 [(메뉴얼 : AV 관리)](https://soju6jan.com/archives/453) <br>
  ○ Plex - JAV Agent 플러그인 추가 <br>
  ○ 파일처리 - AV 플러그인 추가 <br>


##### <span style="color:red">■ 0.1.2 (2019-05-28)</span> #####
- Telegram Bot 플러그인 추가<br>
  [(메뉴얼 : 0.1.2 업데이트 & 텔레그램 봇)](https://soju6jan.com/archives/317) <br>

- 파일처리 - 국내TV 텔레그램 알림 추가


##### <span style="color:red">■ 0.1.1 (2019-05-24)</span> #####
- Plex 플러그인 - 툴 - 쇼 분석 추가<br>
 [(메뉴얼 : PLEX 쇼 분석 사용법 & 정리 팁)](https://soju6jan.com/archives/237)

- Daum TV 플러그인 추가. <br>
  ※ 딱히 플러그인에서 하는 일은 없으며 타 플러그인과 연동<br>
  추후 EPG 및 토렌트 프로그램 플러그인과 연동

##### <span style="color:red">■ 0.1.1 (2019-05-17)</span> #####
- Release
