
<h1 align="center">
  <br>
  백엔드 개발
  <br>
</h1>
<p align="center">
  안드로이드 클라이언트와의 통신을 위한 REST API 기반의 서버 안내
</p>

<p align="center">
  <a href="#prerequisite">Prerequisite</a> •
  <a href="#structure">Structure</a> •
  <a href="#how-to-use">How To Use</a> •
  <a href="#credits">Credits</a> •
  <a href="#other-documents">Other Documents</a> 
</p>

## Prerequisite
**Java 11**이 설치되어 있어야합니다. Spring boot 빌드 툴로 maven을 이용했으나, 프로젝트 내에 maven(mvnw)이 내장되어 있으므로, 추가적인 설치가 요구되진 않습니다.

## Structure

API 관련 코드들은 모두 [controller 폴더](./src/main/java/com/kurly/demo/controller/)에서 확인할 수 있으며, 수정해 이용할 수 있습니다.<br>
데이터베이스와 매칭되는 클래스들은 전부 [model 폴더](./src/main/java/com/kurly/demo/data/)에서 확인할 수 있으며, 수정해 이용할 수 있습니다.<br>
기본 설정과 관련된 파일들은 [config 폴더](./src/main/java/com/kurly/demo/config/)에서 확인할 수 있습니다.

MyBatis의 설정 및 SQL 구문들은 [RSSIMapper 인터페이스](./src/main/java/com/kurly/demo/RSSIMapper.java)와 [myMapper.xml](./src/main/resources/mappers/myMapper.xml)에 정의되어 있습니다. 간단한 SQL은 인터페이스에 어노테이션으로 구현되어있고, 복잡한 동적 쿼리들은 xml 파일에 정의되어있습니다.

## How To Use

To clone and run this application, you'll need [Git](https://git-scm.com) installed on your computer. From your command line:

```bash
# Clone this repository (Password required)
$ git clone https://github.com/backend-project-k.git

# Go into the repository
$ cd backend-project-k

# Make mvnw executable
$ chmod +x mvnw

# Build Program using Maven
$ ./mvnw clean package -DskipTests=true

# Start server
$ java -jar ./target/demo-0.0.1-SNAPSHOT.jar
```

> **Note**
> If you're using Linux Bash for Windows, [see this guide](https://www.howtogeek.com/261575/how-to-run-graphical-linux-desktop-applications-from-windows-10s-bash-shell/).


## Credits

서버 구성에 이용된 프레임워크입니다.

- [Spring Boot](https://spring.io/projects/spring-boot/)
- [MyBatis](https://mybatis.org/mybatis-3/)
- [Swagger](https://swagger.io)

데이터 시각화에 이용된 오픈소스입니다.
- [Grafana](https://grafana.com/)
- [Geoserver](https://geoserver.org/)

## Other Documents

- [Database Schema](./docs/database.md)
- [Grafana 변수](https://grafana.com/docs/grafana/v9.0/variables/variable-types/global-variables/)
