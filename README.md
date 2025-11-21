<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<title>파란 은하수 배경 - 감정 번역기 PPT</title>

<style>
/* ---------------------- 기본 설정 ---------------------- */
body {
    margin: 0;
    padding: 0;
    font-family: 'Apple SD Gothic Neo', Pretendard, sans-serif;
    background: #000;
    color: #fff;
    overflow-x: hidden;
    position: relative;
}

/* 슬라이드 */
section {
    width: 100vw;
    height: 100vh;
    padding: 80px;
    box-sizing: border-box;
    display: none; /* 기본 숨김 */
    flex-direction: column;
    justify-content: center;
    position: relative;
    z-index: 10;
}

section.active {
    display: flex; /* 현재 슬라이드만 보이게 */
}

h1, h2 { margin: 0 0 20px; font-weight: 700; }
h1 { font-size: 48px; }
h2 { font-size: 32px; }

.subtitle { font-size: 20px; margin-bottom: 40px; color: #bcd6ff; }

.box {
    background: rgba(255,255,255,0.1);
    padding: 25px 30px;
    border-radius: 12px;
    margin: 15px 0;
    line-height: 1.55;
    font-size: 20px;
    backdrop-filter: blur(4px);
    border: 1px solid rgba(255,255,255,0.2);
}

.grid-2 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 25px;
}

.qr-box {
    margin-top: 30px;
    padding: 20px;
    background: rgba(80,130,255,0.3);
    border-radius: 10px;
    text-align: center;
    font-size: 20px;
}

footer {
    font-size: 14px;
    text-align: center;
    padding: 40px 0;
    color: #bbb;
    z-index: 50;
}

/* ---------------------- 파란 은하수 배경 ---------------------- */
.nebula {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background: radial-gradient(circle at 30% 40%,
        rgba(150,200,255,0.60) 0%,
        rgba(120,170,255,0.35) 40%,
        rgba(20,40,70,0.50) 70%,
        #000 100%
    );
    filter: blur(60px);
    z-index: 1;
}

/* ---------------------- 별빛 흐르는 효과 ---------------------- */
.stars, .stars2, .stars3 {
    position: fixed;
    top: 0;
    left: 0;
    width: 2px;
    height: 2px;
    background: transparent;
    z-index: 2;
}

/* 별 1층 */
.stars {
    box-shadow:
    1000px 200px #aee2ff, 300px 400px #d7eaff,
    500px 100px #cfe5ff, 700px 900px #ffffff,
    1200px 600px #a7d4ff, 1500px 300px #d1e8ff,
    1800px 800px #bbdbff, 2000px 1200px #e1f1ff,
    900px 1100px #ffffff, 1300px 170px #cfe7ff;

    animation: animStar 60s linear infinite;
}

.stars::after {
    content: "";
    position: absolute;
    top: 2000px;
    width: 2px;
    height: 2px;
    box-shadow:
    1000px 200px #aee2ff, 300px 400px #d7eaff,
    500px 100px #cfe5ff, 700px 900px #ffffff,
    1200px 600px #a7d4ff, 1500px 300px #d1e8ff,
    1800px 800px #bbdbff, 2000px 1200px #e1f1ff,
    900px 1100px #ffffff, 1300px 170px #cfe7ff;
}

/* 별 2층 */
.stars2 {
    box-shadow:
    150px 800px #bbddff, 400px 300px #ffffff, 900px 200px #a6d4ff,
    1200px 900px #c7e2ff, 1800px 400px #ffffff;
    animation: animStar 110s linear infinite;
}

.stars2::after {
    content: "";
    position: absolute;
    top: 2000px;
    width: 2px;
    height: 2px;
    box-shadow:
    150px 800px #bbddff, 400px 300px #ffffff, 900px 200px #a6d4ff,
    1200px 900px #c7e2ff, 1800px 400px #ffffff;
}

/* 별 3층 */
.stars3 {
    box-shadow:
    300px 200px #bbddff, 800px 500px #ffffff,
    1500px 900px #b0d7ff, 400px 1200px #ffffff,
    1700px 700px #e5f4ff;
    animation: animStar 160s linear infinite;
}

.stars3::after {
    content: "";
    position: absolute;
    top: 2000px;
    width: 2px;
    height: 2px;
    box-shadow:
    300px 200px #bbddff, 800px 500px #ffffff,
    1500px 900px #b0d7ff, 400px 1200px #ffffff,
    1700px 700px #e5f4ff;
}

/* 별 흐르는 애니메이션 */
@keyframes animStar {
    from { transform: translateY(0px); }
    to   { transform: translateY(-2000px); }
}

/* ---------------------- 다음 버튼 ---------------------- */
#nextBtn {
    position: fixed;
    bottom: 20px;
    right: 20px;
    padding: 12px 25px;
    font-size: 18px;
    border: none;
    border-radius: 8px;
    background-color: rgba(80,130,255,0.7);
    color: white;
    cursor: pointer;
    z-index: 100;
}
</style>
</head>
<body>

<!-- 파란 은하수 레이어 -->
<div class="nebula"></div>

<!-- 별빛 레이어 -->
<div class="stars"></div>
<div class="stars2"></div>
<div class="stars3"></div>

<!-- ---------------------- 슬라이드 ---------------------- -->
<section>
    <h1>감정 번역기:<br>같은 말, 다른 마음</h1>
    <p class="subtitle">— 귀인이론을 통해 본 메시지 해석의 다양성과 오류 —</p>
    <div class="box">
        같은 상황이나 말도, 사람들은 <b>귀인의 방향</b>에 따라 다르게 해석합니다.<br>
        이 차이는 인간관계에서 오해와 갈등을 만들 수 있습니다.
    </div>
</section>

<section>
    <h2>귀인이론이란?</h2>
    <div class="box">
        사람들은 타인의 행동이나 메시지를 이해할 때 그 원인을 추론(귀인)하려는 경향이 있습니다.
    </div>
    <div class="grid-2">
        <div class="box">
            <h3>① 내부 vs 외부 귀인</h3>
            • 내부: 성격·의도 → ‘그 사람 때문’<br>
            • 외부: 상황·환경 → ‘상황 때문’
        </div>
        <div class="box">
            <h3>② 안정 vs 불안정 귀인</h3>
            • 안정: 지속적/고정적 원인<br>
            • 불안정: 일시적/상황적 원인
        </div>
    </div>
</section>

<section>
    <h2>4가지 귀인 유형 요약</h2>
    <div class="grid-2">
        <div class="box"><b>내부 + 안정</b><br>“그 애는 원래 나한테 무관심해.”<br>→ 관계 위협감 증가</div>
        <div class="box"><b>내부 + 불안정</b><br>“지금 나에게 실망한 것 같아.”<br>→ 자책·감정적 반응</div>
        <div class="box"><b>외부 + 안정</b><br>“요즘 바빠서 그래.”<br>→ 상황 이해</div>
        <div class="box"><b>외부 + 불안정</b><br>“오늘만 타이밍이 안 맞았어.”<br>→ 융통성 있음</div>
    </div>
</section>

<section>
    <h2>상황 1: 연애 메시지 해석</h2>
    <div class="box">영상 영역</div>
    <div class="box">
        1. “내가 매력이 없나?”<br>
        2. “내가 말투를 잘못 보냈나?”<br>
        3. “원래 무뚝뚝한 사람이야.”<br>
        4. “오늘 피곤했겠지.”
    </div>
    <div class="qr-box">📌 지금 QR을 찍고 설문조사에 참여해주세요!</div>
</section>

<section>
    <h2>해석 유형 설명</h2>
    <div class="grid-2">
        <div class="box"><b>내부-안정</b><br>자신감 ↓, 표현 감소</div>
        <div class="box"><b>내부-불안정</b><br>후회 → 행동 수정</div>
        <div class="box"><b>외부-안정</b><br>짜증·거리두기</div>
        <div class="box"><b>외부-불안정</b><br>자연스럽게 넘어감</div>
    </div>
</section>

<section>
    <h2>상황 2: 친구 지각</h2>
    <div class="box">영상 영역</div>
    <div class="box">
        1. “원래 시간 개념이 없지.”<br>
        2. “오늘 늦게 준비했나?”<br>
        3. “그 지역은 원래 막혀.”<br>
        4. “오늘 비 와서 늦었겠지.”
    </div>
    <div class="qr-box">📌 지금 QR을 찍고 설문조사에 참여해주세요!</div>
</section>

<section>
    <h2>해석 유형 설명</h2>
    <div class="grid-2">
        <div class="box"><b>내부-안정</b><br>친구 성향 탓</div>
        <div class="box"><b>내부-불안정</b><br>일시적 실수</div>
        <div class="box"><b>외부-안정</b><br>환경적 요인</div>
        <div class="box"><b>외부-불안정</b><br>하루의 변수</div>
    </div>
</section>

<section>
    <h2>상황 3: 교수님 피드백</h2>
    <div class="box">
        1. “나는 원래 실력이 부족해서…”<br>
        2. “오늘 대충 발표했나?”<br>
        3. “교수님 원래 스타일이지.”<br>
        4. “오늘 교수님 기분 좋으신가보네.”
    </div>
</section>

<section>
    <h2>해석 유형 설명</h2>
    <div class="grid-2">
        <div class="box"><b>내부-안정</b><br>위축, 감정적 추리 주의</div>
        <div class="box"><b>내부-불안정</b><br>개선 행동으로 연결</div>
        <div class="box"><b>외부-안정</b><br>말투 스타일로 이해</div>
        <div class="box"><b>외부-불안정</b><br>컨디션 해석</div>
    </div>
</section>

<footer>© 감정 번역기 PPT (HTML/CSS)</footer>

<!-- ---------------------- 다음 버튼 ---------------------- -->
<button id="nextBtn">다음 ▶</button>

<script>
// ---------------------- 슬라이드 JS ----------------------
const slides = document.querySelectorAll('section');
const nextBtn = document.getElementById('nextBtn');
let currentSlide = 0;

// 처음 슬라이드 보여주기
slides[currentSlide].classList.add('active');

nextBtn.addEventListener('click', () => {
    slides[currentSlide].classList.remove('active'); // 현재 슬라이드 숨기기
    currentSlide++;
    if (currentSlide >= slides.length) currentSlide = 0; // 마지막 슬라이드 다음은 첫 슬라이드
    slides[currentSlide].classList.add('active'); // 새 슬라이드 표시
});
</script>

</body>
</html>
