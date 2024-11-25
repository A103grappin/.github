# 🧷 Grappin

![grappin_logo.png](docs/assets/grappin_logo.svg)

> 손쉬운 협업을 위한 **영상 정보 공유 플랫폼**

---

## 🗂️ 서비스 소개

|![monthly_active_users_on_YouTube](./docs/assets/monthly_active_users_on_YouTube.png)|
|:--:|
|출처: https://www.charleagency.com/articles/youtube-statistics/|


 영상 콘텐츠는 나날이 증가하고 있습니다. 이런 환경에서 개인과 팀이 방대한 정보를 체계적으로 관리하기 위한 도구는 필수적이라고 할 수 있습니다.

우리가 일반적으로 사용하는 키워드 기반 검색은 영상 매체에서 큰 효과를 발휘하지 못합니다. 영상 데이터를 잘 관리하기 위해서는 적절한 집약뿐만 아니라 탐색 또한 손쉽게 이뤄져야 할 것입니다.

 Grappin은 워크스페이스에서 유튜브 영상을 자유롭게 공유하고, RAG가 적용된 챗봇을 통해 원하는 영상을 손쉽게 찾도록 합니다.

---


## ⚙ 주요 기능

### 📂 워크스페이스 및 팀원 관리

 Grappin에서는 워크스페이스 단위로 작업을 진행합니다. 사이드바에서 자신이 소속된 워크스페이스 목록을 확인하고 팀원 정보, 초대 링크를 확인할 수 있습니다.

![workspace.gif](docs/assets/workspace.gif)

---

### 🎬 영상(게시글) 등록

 유튜브 영상의 url을 입력하여 워크스페이스에 영상을 등록할 수 있습니다. 또한 태그를 추가하여 부가적인 정보를 더할 수도 있습니다.

![add_post.gif](docs/assets/add_post.gif)

---

### 📝 게시글 요약본 조회 & 메모장 작성

 게시글 등록을 요청하면 FastAPI에서 영상 스크립트를 기반으로 LLM을 통해 요약본을 생성하고, 챗봇에 활용할 수 있도록 임베딩을 합니다. 요약본 생성이 완료되면 게시글 상세 조회에서 내용을 확인할 수 있습니다.

![video_summary.gif](docs/assets/video_summary.gif)

 메모장에서는 영상에 대한 종합적인 의견을 작성합니다. 메모장은 [yorkie 라이브러리](https://yorkie.dev/)를 기반으로 실시간 동시 편집이 가능합니다.

![collaborative_real-time_editor.gif](docs/assets/collaborative_real-time_editor.gif)

---

### 💬 타임카드

 게시글 영상의 특정 구간에 대한 코멘트를 남기고 싶하면 타임카드를 이용하면 됩니다.

 현재 내가 보고 있는 시점에 대해 짧은 문구와 함께 타임카드를 남길 수 있습니다. 다른 사람의 타임카드를 클릭하면 해당 구간을 바로 시청할 수 있습니다.

<table>
    <tr>
        <td align="center">
            <img src="./docs/assets/timecard_01.gif" alt="팀원이 남긴 타임카드 보기" >
            <p><strong>팀원이 남긴 타임카드 보기</strong></center></p>
        </td>
        <td align="center">
            <img src="./docs/assets/timecard_02.gif" alt="타임카드 추가하기" >
            <p><strong>타임카드 추가하기</strong></center></p>
        </td>
        <td align="center">
            <img src="./docs/assets/timecard_03.gif" alt="팀원별 타임카드 보기" >
            <p><strong>팀원별 타임카드 보기</strong></center></p>
        </td>
    </tr>
</table>

---

### 🤖 챗봇을 이용한 영상 자료 검색

 영상 매체는 검색이 어렵습니다. 영상 제목, 채널 이름이 기억나지 않는다면 검색의 어려움은 더더욱 커집니다. Grappin에서는 RAG를 통해 이런 어려움을 해결하였습니다.

 워크스페이스에 영상을 추가하면 유튜브의 스크립트를 가져와 벡터화합니다. 문맥과 의미를 기반으로 유사성을 평가하여 더 정확한 검색 결과를 제공합니다. 질문에 대한 영상, 시점 뿐만 아니라 검색 결과에 대한 근거를 함께 제시해, 신뢰성을 강화하고 사용자가 필요로 하는 내용을 빠르게 활용할 수 있도록 지원합니다.

![chatbot.gif](docs/assets/chatbot.gif)

---

### 🧩 크롬 익스텐션

 Grappin은 크롬 익스텐션을 통해 영상을 손쉽고 빠르게 관리할 수 있도록 하였습니다. 유튜브에서 원하는 영상을 발견하였다면 우측의 요소를 통해 요약문을 확인하고 워크스페이스에 바로 추가할 수 있습니다.

![chrome_extension.gif](docs/assets/chrome_extension.gif)

---

## 🛠️ 아키텍처

![Grappin_Architecture.png](docs/assets/Grappin_Architecture.png)

---

## 🔧 기술 스택

### 🖥️ FrontEnd
<!-- [![My Skills](https://skillicons.dev/icons?i=react,vite,js,styledcomponents,vscode)](https://skillicons.dev) -->
<img src="https://img.shields.io/badge/react-61DAFB?style=for-the-badge&logo=react&logoColor=white">
<img src="https://img.shields.io/badge/vite-646CFF?style=for-the-badge&logo=vite&logoColor=white">
<img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=white">
<img src="https://img.shields.io/badge/styled-components-DB7093?style=for-the-badge&logo=styled-components&logoColor=white">

### 🌐 BackEnd
<!-- [![My Skills](https://skillicons.dev/icons?i=java,spring,python,fastapi,express,idea)](https://skillicons.dev) -->
<img src="https://img.shields.io/badge/java-4479A1?style=for-the-badge&logo=java&logoColor=white">
<img src="https://img.shields.io/badge/springboot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white">
<img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white">
<img src="https://img.shields.io/badge/fastapi-009688?style=for-the-badge&logo=fastapi&logoColor=white">
<img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=white">
<img src="https://img.shields.io/badge/express-000000?style=for-the-badge&logo=express&logoColor=white">
<img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white">
<img src="https://img.shields.io/badge/mongodb-47A248?style=for-the-badge&logo=mongodb&logoColor=white">

### 🤖 AI
<img src="https://img.shields.io/badge/Langchain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white">
<img src="https://img.shields.io/badge/openai_text_embedding_ada_002-412991?style=for-the-badge&logo=openai&logoColor=white">
<img src="https://img.shields.io/badge/openai_gpt_4o-412991?style=for-the-badge&logo=openai&logoColor=white">
<img src="https://img.shields.io/badge/faiss-0467DF?style=for-the-badge&logo=meta&logoColor=white">

---

## 👥 팀원
<table>
    <tr>
        <td align="center">
            <a href="https://lab.ssafy.com/kang99086"><img src="https://secure.gravatar.com/avatar/dc130ac71df20ffc71041dd6eba3c9fb6d1675ddb787c0ea76d00cb85aa8a163?s=384&d=identicon" width=160/></a>
        </td>
        <td align="center">
            <a href="https://lab.ssafy.com/rara0620"><img src="https://secure.gravatar.com/avatar/03f7ddd9646025622f705832b9e70f3a9f8ba9a8120f38d638f3f2b482cb84f6?s=384&d=identicon" width=160/></a>
        </td>
        <td align="center">
            <a href="https://lab.ssafy.com/sjiyeon759"><img src="https://lab.ssafy.com/uploads/-/system/user/avatar/17451/avatar.png?width=192" width=160/></a>
        </td>
    </tr>
    <tr>
        <td align="center">
            <strong>강민제</strong>
            <br>
            FE, BE, Chrome Extension
            </br>
        </td>
        <td align="center">
            <strong>류성윤</strong>
            <br>
            RAG, FE
            </br>
        </td>
        <td align="center">
            <strong>신지연</strong>
            <br>
            UI/UX design, BE, 실시간 동시편집
            </br>
        </td>
    </tr>
        <tr align="center">
        <td>
            <a href="https://lab.ssafy.com/liveinmars2018"><img src="https://secure.gravatar.com/avatar/a01827b0091d84ddc0fa2936c7e0ca8f70c9881a4c7d9f402f92d65f0b26ebd1?s=384&d=identicon" width=160/></a>
        </td>
        <td align="center">
            <a href="https://lab.ssafy.com/hyndrome"><img src="https://secure.gravatar.com/avatar/2eb1de5908b47b448a299f02cd0315fe9c42dd290893b52ff3a7948b8e9d0a1a?s=384&d=identicon" width=160/></a>
        </td>
        <td>
            <a href="https://lab.ssafy.com/dydgustm"><img src="https://secure.gravatar.com/avatar/b4421bf4a0c7404394c67c40b1e809771a6d2f766fe8877e843248f8f1d4c574?s=384&d=identicon" width=160/></a>
        </td align="center">
    </tr>
    <tr>
        <td align="center">
            <strong>이현주</strong>
            <br>
            PM, FE, BE, Infra
        </td>
        <td align="center">
            <strong>진홍엽</strong>
            <br>
            FE, Chrome Extension
        </td>
        <td align="center">
            <strong>최용현</strong>
            <br>
            BE, 실시간 동시편집
        </td>
    </tr>
</table>
