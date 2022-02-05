<h3 align="center"><b>📰 (전국) 2021 ICT 융합 프로젝트 공모전 / 우수상 📰</b></h3>
<h4 align="center">📆 2021.03.01 ~ 2021.03.10</h4>
<br>

---

<h3><b>🎫 프로젝트 소개 🎫</b></h3>
노약자나 거동이 불편한 사람들에게 편리한 쇼핑 환경을 제공해 주기 위해 
<br>최적 경로 길 안내, 자동 결제 시스템 등이 탑재된 스마트 쇼핑 카트이다.

<br>
<h3><b>👨🏻‍🤝‍👨🏻 Members 👨🏻‍🤝‍👨🏻</b></h3>
팀장 : 양성은
<br>팀원 : 김형덕, 박유나, 이유진

---

<h3><b>🛠 Tech Stack 🛠</b></h3>
<p>
<img src="https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white">
<img src="https://img.shields.io/badge/RaspberryPi-FC5230?style=for-the-badge&logo=RaspberryPi&logoColor=white">
<img src="https://img.shields.io/badge/Android-7DB249?style=for-the-badge&logo=Android&logoColor=white">
<img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white"/>
<img src="https://img.shields.io/badge/Python-1F497D?style=for-the-badge&logo=Python&logoColor=white">
</p>

<br><br>
<h3><b>📢 Entity Relationship Diagram 📢</b></h3>


<br><br>

---

<h3><b>1️⃣ 기능블록도</b></h3>
<img src="https://user-images.githubusercontent.com/57797592/152631271-01248071-5d01-474d-a01f-f9a32be4a5cb.png" />

<br><br>
<h3><b>2️⃣ 전체 시스템 구성</b></h3>
<img src="https://user-images.githubusercontent.com/57797592/152631195-dca60a13-46f4-4822-953a-007779e4900f.png" />

<br><br>
<h3><b>3️⃣ 동작 흐름도</b></h3>
<img src="https://user-images.githubusercontent.com/57797592/152631256-cd276608-0a14-4996-8398-10f3b6e860f8.png" />

<br><br>
<h3><b>🏷 주요 기능 🏷</b></h3>
<h4><b>📰 Barcode scan을 통한 상품, 장바구니 database 구성 📰</b></h4>
<h4><b>📰 Barcode scan을 통한 행사 정보 음성 안내 기능 TTS 구현  📰</b></h4>
<table width="100%">
    <tr>
        <td width="50%"><img src="https://user-images.githubusercontent.com/57797592/152631488-6b3ff8b9-2929-41f1-abec-46c0b95e640d.png" /></td>
        <td width="50%">
            <ul>
                <li>상품의 바코드를 스캔하면 자동으로 장바구니 목록에 추가 됨</li>
                <li>스캔한 상품에 행사 정보가 존재할 경우 사용자에게 음성 안내 출력<br>Ex) 1+1 행사 상품입니다.</li>
                <li>카트에 달린 모니터로 장바구니 목록을 확인 가능하고 모니터 터치를 통해 목록 수정 또한 가능</li>
            </ul>
        </td>
    </tr>
</table>

<br>
<h4><b>📰 RF통신과 삼변측량법을 통한 실내 위치 측위 📰</b></h4>
<table width="100%">
    <tr>
        <td width="50%"><img src="https://user-images.githubusercontent.com/57797592/152631690-b6b08a54-96d2-4923-bffa-03747ad235f4.png" /></td>
        <td width="50%">
            <ul>
                <li>RF Beacon을 통해 얻은 RSSI 값으로 직선 거리를 구함(3개의 비콘 직선거리를 모두 가져와야 한다.)</li>
                <li>얻은 직선거리를 삼변 측량법 알고리즘을 통해 사용자의 현재 위치 값을 얻어온다.</li>
            </ul>
        </td>
    </tr>
</table>

<br>
<h4><b>📰 TSP algorithm을 통한 최단경로 추적 📰</b></h4>
<table width="100%">
    <tr>
        <td width="50%"><img src="https://user-images.githubusercontent.com/57797592/152631776-d9cc345d-e90e-4daa-b8cf-486b6b35ffb4.png" /></td>
        <td width="50%">
            <ul>
                <li>TSP algorithm을 사용하여 사용자가 선택한 코너를 모두 1번 씩 들릴 때 최단 경로를 구한다.</li>
                <li>카트에 부착된 모니터로 사용자에게 경로를 보여준다.</li>
            </ul>
        </td>
    </tr>
</table>

<br>
<h4><b>📰 부트페이 인 앱 결제 어플리케이션 📰</b></h4>
<table width="100%">
    <tr>
        <td width="50%"><img src="https://user-images.githubusercontent.com/57797592/152631802-a5a885d8-59b7-4c0f-8c44-687c1e988a0e.png" /></td>
        <td width="50%">
            <ul>
                <li>카트에 구성된 품목의 총 합을 계산하여 어플로 전달한다.</li>
                <li>전달된 가격을 부트페이 인 앱 결제로 결제화면을 사용자에게 띄워준다.</li>
            </ul>
        </td>
    </tr>
</table>
<br>

---

<h3 align="center"><b>✏ Trouble Shooting ✏</b></h3>
<br>
<details>
    <summary>
        <b>실내 위치 측위에서 Bluetooth Beaon을 사용했을 때 RSSI 값의 오차가 너무 큰 문제 발생</b>
    </summary>
    <br>해결 : RF Beacon으로 바꾸어 반경 거리 확대, 오차 범위 감소
    <br>자세히 보기 : https://indecisive-viscount-244.notion.site/f5b12e26bdf84cb1b2fa2e4f312aec67
</details>
