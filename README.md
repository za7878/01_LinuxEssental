Linux Essental 과정 정리

제 01장. Linux Command
제 02장. Directory Administration

Linux 관리자 과정
* Linux 기초 관리자 과정 (8일)
* Linux 서버 관리자 과정 (2일)
* Linux 서비스/보안 관리자 과정 (8일)


Linux 기초 관리자 과정

자격증
* 민간 자격증
* 국가 자격증
	ㄴ> 리눅스 마스터 1급/2급
	    네트워크 관리사 1급/2급
		
		정보처리기사
* 국제 공인 자격증
	AWS SA
	★ RedHat RHCSA/RHCE ★
	LPIC
	
	
복제된 운영체제에서 변경 사항
* 호스트 이름
	# hostnamectl
	# hostnamectl set-hostname server1.example.com
* IP 설정
	# nm-connection-editor
	# nmcli connection up <Porfile>
-- 바꾸는 이유는 이름과 ip가 같으면, 충돌이 나기 때문.


용어(Terms)
* TUI (Text User Interface), CLI(Command Line Interface)
* GUI (Graphic User Interface)

동작수준/동작레벨 (RunLevel) == 대상(Target)
-- 명칭만 바뀌었을 뿐. 현재는 Target 이라고 함.



리눅스의 선수지식
* runLevel == Target
	runLevel 3 == multi-user.target
	runLevel 5 == graphical.target
	
		# systemctl isolate multi-user.target || graphical.target
		# systemctl set-default multi-user.target || graphical.target
		
* 서비스 기동
	# systemctl enable || disable firewalld
	# systemctl start || stop firewalld
	
* 제어 문자(Control Character)
	# <CTRL + C>, <CTRL + D>
	-- CTRL + C는, 현재 실행중인 동작 강제 종료
	-- CTRL + D는, (ㄱ) 파일의 끝(EOF), (ㄴ) 현재 쉘 종료.
