# kafka-demo
###사용 환경
1. jdk 1.8 
2. gradle
3. spring boot 2.2.6
4. mybatis
5. swagger 2.9
6. h2db (in-memory)
7. kafka_2.12-2.1.1 (https://archive.apache.org/dist/kafka/2.1.1/kafka_2.12-2.1.1.tgz)

###개발환경 구성
1. git clone <url> 으로 개발소스 복제
2. kafka 다운로드
3. kafka 설정
   1. %KAFKA_HOME%\config\ 폴더에 있는 zookeeper.properties 파일을 열어 dataDir=/tmp/zookeeper 항목을 dataDir=C:/temp/zookeeper 로 변경

###프로그램 빌드
1. 전체 프로젝트 빌드
   gradlew build
2. 모듈별 빌드
   gradlew :<모듈명>:build

###프로그램 실행
1. zookeeper 실행
   1. 새로운 윈도우 코맨드 창을 열어 kafka가 설치된 디렉토리로 이동
   2. 윈도우라면 다음과 같이 bin\windows\zookeeper-server-start.bat를 실행
   3. 이때 입력 파라미터로 %KAFKA_HOME%\config\zookeeper.properties의 경로명과 파일명을 함께 넘길 것
   4. e.g. start/b C:\kafka_2.12-2.1.1\bin\windows\zookeeper-server-start.bat C:\kafka_2.12-2.1.1\config\zookeeper.properties
2. kafka 실행
   1. 새로운 윈도우 코맨드 창을 열어 kafka가 설치된 디렉토리로 이동 
   2. 윈도우라면 다음과 같이 bin\windows\kafka-server-start.bat를 실행
   3. 이떄 입력 파라미터로 %KAFKA_HOME%\config\server.properties를 넘길 것
   4. e.g. start/b C:\kafka_2.12-2.1.1\bin\windows\kafka-server-start.bat C:\kafka_2.12-2.1.1\config\server.properties
3. kafka-demo/kafka-pub/src/main/java/KafkaPubApplication을 찾아 실행
4. kafka-demo/kafka-sub/src/main/java/KafkaSubApplication을 찾아 실행

### 프로그램 테스트
1. http://localhost:8080/pub/swagger-ui.html 호출
   1. 
