# TFTPClient
TFTP 클라이언트
이 프로젝트는 Python으로 구현된 간단한 TFTP 클라이언트입니다. 
TFTP는 클라이언트와 서버 간에 파일을 전송하는 데 사용되는 간단한 프로토콜입니다.

사용 예제)
파일 업로드 (PUT): python3 tftpcl.py(파이썬 파일) 203.250.133.88 put text.txt(텍스트 파일)
파일 다운로드 (GET): python3 tftpcl.py(파이썬 파일) 203.250.133.88 get text.txt(텍스트 파일)

구현 세부 정보
이 스크립트는 TFTP 서버와의 연결을 수립하기 위해 Python의 socket 라이브러리를 사용하며 파일 전송을 위한 TFTP 프로토콜을 구현합니다.

지원되는 작업
Read Request (RRQ)
Write Request (WRQ)
Data Transfer (DATA)
Acknowledgment (ACK)
Error (ERROR)

오류 처리
클라이언트는 다양한 TFTP 오류를 처리하며 해당 오류 메시지를 표시합니다.
0: "Not defined, see error message (if any).",
1: "File not found.",
2: "Access violation.",
3: "Disk full or allocation exceeded.",
4: "Illegal TFTP operation.",
5: "Unknown transfer ID.",
6: "File already exists.",
7: "No such user."

참고 사항
타임아웃을 포함하고 있습니다.
올바른 명령어(put 또는 get)를 입력하지 않았을 경우 올바른 명령어를 입력하라는 문구를 표시합니다.
