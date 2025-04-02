# 🧱☁️ Newspace MSA & Cloud Deployment Project

25.03.27 ~ 25.04.02

LG CNS AM Inspire Camp 1기

미니프로젝트 2 - 9조

<table>
    <tr>
        <!-- 첫 번째 팀원 -->
        <td align="center" width="20%">
            <img src="https://avatars.githubusercontent.com/u/151743721?v=4" alt="Avatar" width="100px"/><br/>
            <a href="https://github.com/95hyun">현민영(팀장)</a>
            <br/>
            <img src="https://github-readme-stats.vercel.app/api?username=95hyun&show_icons=true&theme=transparent" alt="95hyun's GitHub stats" width="300px"/>
            <br/>
            Monolithic -> MSA 리팩토링
            <br>
            Prometheus, Grafana 구현
            <br>
            Grafana Alert Discord Webhook
        </td>
        <!-- 두 번째 팀원 -->
        <td align="center" width="20%">
            <img src="https://avatars.githubusercontent.com/u/39462045?v=4" alt="Avatar" width="100px"/><br/>
            <a href="https://github.com/dhku">구동혁</a>
            <br/>
            <img src="https://github-readme-stats.vercel.app/api?username=dhku&show_icons=true&theme=transparent" alt="dhku's GitHub stats" width="300px"/>
            <br/>
            CI/CD docker-compose, 
            <br>
            무중단 배포,
            <br>
            CI/CD 자동화 구축 및 개선 
        </td>
        <!-- 세 번째 팀원 -->
        <td align="center" width="20%">
            <img src="https://avatars.githubusercontent.com/u/84431156?v=4" alt="Avatar" width="100px"/><br/>
            <a href="https://github.com/js4939">김지수</a>
            <br/>
            <img src="https://github-readme-stats.vercel.app/api?username=js4939&show_icons=true&theme=transparent" alt="js4939's GitHub stats" width="300px"/>
            <br/>
            프론트엔드 Jenkins 파이프라인 구성 및 CI/CD, 
            <br>
            요구사항 명세서 작성, 
            <br>
            프론트엔드 & 백엔드 연동
        </td>
        <!-- 네 번째 팀원 -->
        <td align="center" width="20%">
            <img src="https://avatars.githubusercontent.com/u/140885810?v=4" alt="Avatar" width="100px"/><br/>
            <a href="https://github.com/woogieon8on">박상욱</a>
            <br/>
            <img src="https://github-readme-stats.vercel.app/api?username=woogieon8on&show_icons=true&theme=transparent" alt="woogieon8on's GitHub stats" width="300px"/>
            <br/>
            Config 서버 + RabbitMQ, 
            <br>
            docker 일부 AWS 전환 + EC2 + RDS
        </td>
        <!-- 다섯 번째 팀원 -->
        <td align="center" width="20%">
            <img src="https://avatars.githubusercontent.com/u/95837534?v=4" alt="Avatar" width="100px"/><br/>
            <a href="https://github.com/Y0ungse">유영서</a>
            <br/>
            <img src="https://github-readme-stats.vercel.app/api?username=Y0ungse&show_icons=true&theme=transparent" alt="Y0ungse's GitHub stats" width="300px"/>
            <br/>
            프론트엔드 배포, 
            <br>
            서비스 아키텍처 다이어그램 작성, 
            <br>
            PPT
        </td>
    </tr>
</table>
<br/>

---

<br/>

## 📌 프로젝트 개요

**Newspace**는 확장성과 유연성을 중심으로 설계된 **모듈형 뉴스 플랫폼**입니다.  
Spring Cloud 기반의 마이크로서비스 아키텍처(MSA)와 React 프론트엔드를 사용하여,  
각 서비스가 **독립적으로 배포·운영 가능한 구조**로 구성되어 있습니다.

CI/CD는 GitHub → Jenkins → Docker Compose 기반으로 자동화되어 있으며,  
프론트엔드는 S3에 배포되고 CloudFront를 통해 정적 자원을 빠르게 서빙합니다.  
API 요청은 CloudFront를 통한 **리버스 프록시 방식**으로 처리되어, 
쿠키 기반 인증도 안정적으로 동작합니다.

백엔드는 Eureka 기반의 Service Discovery와 Spring Cloud Gateway를 통해 유기적으로 연결되며,  
각 마이크로서비스는 **Blue-Green 배포 전략**을 적용해 무중단 배포를 지원합니다.   
데이터는 AWS RDS(MariaDB)에 저장되며,  
뉴스 서비스는 **Spring AI**를 통해 Groq 기반의 Deepseek LLM과 연동되어 뉴스 요약 기능을 제공합니다.

또한 Prometheus와 Grafana를 통해 **서비스 상태를 실시간으로 모니터링**할 수 있도록 구성되어 있습니다.

<br/>

## 🛠️ 기술 스택

### 🖥️ Frontend
<img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=HTML5&logoColor=white"> <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=CSS3&logoColor=white"> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScript&logoColor=black"> <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=React&logoColor=black"> <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=Vite&logoColor=white"> <img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=Figma&logoColor=white">

### ⚙️ Backend
<img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=SpringBoot&logoColor=white"> <img src="https://img.shields.io/badge/Spring%20Security-6DB33F?style=for-the-badge&logo=SpringSecurity&logoColor=white"> <img src="https://img.shields.io/badge/Spring%20Cloud-6DB33F?style=for-the-badge&logo=Spring&logoColor=white"> <img src="https://img.shields.io/badge/Spring%20AI-6DB33F?style=for-the-badge&logo=Spring&logoColor=white"> <img src="https://img.shields.io/badge/Spring%20WebFlux-6DB33F?style=for-the-badge&logo=SpringWebFlux&logoColor=white"> <img src="https://img.shields.io/badge/Gradle-02303A?style=for-the-badge&logo=Gradle&logoColor=white"> <img src="https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=MariaDB&logoColor=white">

### ☁️ DevOps & Infra
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=white"> <img src="https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=Jenkins&logoColor=white"> <img src="https://img.shields.io/badge/GitHub_Webhook-181717?style=for-the-badge&logo=github&logoColor=white"> <img src="https://img.shields.io/badge/NGINX-009639?style=for-the-badge&logo=NGINX&logoColor=white"> <img src="https://img.shields.io/badge/AWS_EC2-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white"> <img src="https://img.shields.io/badge/AWS_RDS-527FFF?style=for-the-badge&logo=amazonaws&logoColor=white"> <img src="https://img.shields.io/badge/AWS_S3-569A31?style=for-the-badge&logo=amazonaws&logoColor=white"> <img src="https://img.shields.io/badge/AWS_CloudFront-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white">

### 📊 Monitoring
<img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white"> <img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white">
  
### 🧪 API & Collaboration
<img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=Postman&logoColor=white"> <img src="https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=Swagger&logoColor=white"> <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=Notion&logoColor=white">

<br/>

## 🚀 배포 주소

👉 [NewSpace 프론트엔드 배포 링크](http://d1wvssrshiud2m.cloudfront.net)

> 위 링크를 통해 실제 서비스된 프론트엔드 앱을 확인할 수 있습니다.

<br/>

## 📂 Repository Overview
### 🔧 Infrastructure
- [`newspace-config`](https://github.com/newspace-msa/newspace-config): 공통 설정 저장소
- [`newspace-config-service`](https://github.com/newspace-msa/newspace-config-service): Config Server
- [`newspace-eureka`](https://github.com/newspace-msa/newspace-eureka): Service Registry (Eureka)
- [`newspace-gateway`](https://github.com/newspace-msa/newspace-gateway): API Gateway

### 🧩 Domain Services
- [`newspace-user-service`](https://github.com/newspace-msa/newspace-user-service): 사용자 서비스
- [`newspace-notice-service`](https://github.com/newspace-msa/newspace-notice-service): 공지사항 서비스
- [`newspace-news-service`](https://github.com/newspace-msa/newspace-news-service): 뉴스 관리 서비스

### 🌐 Frontend
- [`newspace-frontend`](https://github.com/newspace-msa/newspace-frontend): React 기반 프론트엔드

### 🚀 Deployment
- [`newspace-deploy`](https://github.com/newspace-msa/newspace-deploy): 배포 자동화 스크립트 및 문서

<br/>

## 🏗️ 시스템 아키텍처
![image](https://github.com/user-attachments/assets/bba4aae7-b01a-46dc-8aee-096fa4736107)

<br/>

## 🗺️ 서비스 간 통신 흐름

사용자의 요청은 다음과 같은 흐름으로 처리됩니다:

### 1. 클라이언트 요청

- 사용자는 브라우저(React/Vite 프론트엔드)에서 `/api/*` 경로로 API를 요청합니다.  
- 해당 요청은 CloudFront를 통해 전달되며, 리버스 프록시 설정을 통해 API Gateway로 전송됩니다.

### 2. API Gateway

- Spring Cloud Gateway는 클라이언트 요청을 받아 내부 마이크로서비스로 라우팅합니다.  
- 라우팅 기준은 Eureka에 등록된 서비스 이름과 경로(prefix)를 기반으로 결정됩니다.

### 3. Service Discovery

- Gateway는 Eureka Service Discovery를 통해 각 마이크로서비스 인스턴스를 조회합니다.  
- 모든 마이크로서비스는 자신의 상태와 포트를 Eureka에 주기적으로 등록 및 갱신합니다.

### 4. 도메인 서비스 처리

- 요청은 해당 도메인의 Spring Boot 기반 마이크로서비스로 전달되어 비즈니스 로직을 처리합니다.

|     예시 요청    |    처리 서비스   |
| ----------------- | ---------------- |
| 사용자 로그인     | `user-service`   |
| 공지 목록 조회    | `notice-service` |
| 뉴스 데이터 요청  | `news-service`   |

### 5. AI 요약 처리

- 뉴스 요약 요청의 경우, `news-service`는 내부적으로 Spring AI를 통해  
  Groq + Deepseek 기반 LLM과 연동하여 요약 결과를 생성합니다.

### 6. 응답 반환

- 처리된 응답은 다시 API Gateway를 거쳐 프론트엔드로 전달됩니다.  
- 사용자의 브라우저에서 결과가 렌더링되어 표시됩니다.

<br/>

## 📚 Notion
https://www.notion.so/LG-CNS-2-9-1c35254cd71680b490c6f7d3a8a0b2e6
