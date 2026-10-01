<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Yêu Phương Anh 🌸</title>

<style>

/* =========================
   CÀI ĐẶT CHUNG
========================= */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    min-height: 100vh;
    overflow: hidden;

    font-family: "Segoe UI", sans-serif;

    background:
        radial-gradient(
            circle at 50% 40%,
            #fff8fc 0%,
            #ffd9e9 30%,
            #bde8df 70%,
            #8ccfc5 100%
        );

    color: #b82f68;
}


/* =========================
   ÁNH SÁNG NỀN
========================= */

body::before {
    content: "";

    position: fixed;

    width: 650px;
    height: 650px;

    left: 50%;
    top: 45%;

    transform: translate(-50%, -50%);

    background: rgba(255,255,255,0.35);

    border-radius: 50%;

    filter: blur(80px);

    pointer-events: none;
}


/* =========================
   KHUNG TRANG
========================= */

.page {
    position: relative;

    width: 100%;
    min-height: 100vh;

    display: flex;
    align-items: center;
    justify-content: center;

    padding: 20px;
}


/* =========================
   KHUNG KÍNH
========================= */

.card {

    position: relative;

    width: min(760px, 92vw);

    min-height: 600px;

    padding: 60px 45px;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    text-align: center;

    background: rgba(255,255,255,0.30);

    backdrop-filter: blur(18px);

    border:

        2px solid
        rgba(255,255,255,0.7);

    border-radius: 45px;

    box-shadow:

        0 30px 80px
        rgba(93, 166, 158, 0.25),

        inset 0 0 40px
        rgba(255,255,255,0.25);

    z-index: 10;

    animation: appear 1.5s ease;
}


@keyframes appear {

    from {
        opacity: 0;
        transform: translateY(30px) scale(.9);
    }

    to {
        opacity: 1;
        transform: translateY(0) scale(1);
    }
}


/* =========================
   HOA TRÊN
========================= */

.top-flowers {

    font-size: 42px;

    letter-spacing: 10px;

    margin-bottom: 20px;

    animation: sway 3s infinite ease-in-out;
}


@keyframes sway {

    0%,100% {
        transform: rotate(-2deg);
    }

    50% {
        transform: rotate(2deg);
    }
}


/* =========================
   TIÊU ĐỀ
========================= */

.title {

    font-size: clamp(40px, 7vw, 72px);

    font-weight: 800;

    background:
        linear-gradient(
            90deg,
            #d82f70,
            #f27ca8,
            #55a99e,
            #d82f70
        );

    background-size: 300%;

    -webkit-background-clip: text;

    color: transparent;

    animation: gradient 5s infinite linear;

    text-shadow:
        0 5px 25px
        rgba(216,47,112,.15);
}


@keyframes gradient {

    0% {
        background-position: 0%;
    }

    100% {
        background-position: 300%;
    }
}


/* =========================
   DÒNG PHỤ
========================= */

.subtitle {

    margin-top: 12px;

    color: #527f79;

    font-size: 18px;

    letter-spacing: 2px;
}


/* =========================
   TRÁI TIM
========================= */

.heart-box {

    margin: 40px 0;

    position: relative;

    width: 160px;
    height: 160px;

    display: flex;
    align-items: center;
    justify-content: center;
}


.heart {

    position: relative;

    width: 110px;
    height: 110px;

    background:
        linear-gradient(
            135deg,
            #ff7fae,
            #d92e6b
        );

    transform: rotate(-45deg);

    border-radius: 15px;

    box-shadow:

        0 0 25px #ff91b7,

        0 0 60px
        rgba(255,96,151,.5);

    animation: beat 1.4s infinite;
}


.heart::before,
.heart::after {

    content: "";

    position: absolute;

    width: 110px;
    height: 110px;

    background: inherit;

    border-radius: 50%;
}


.heart::before {

    top: -55px;
    left: 0;
}


.heart::after {

    left: 55px;
    top: 0;
}


@keyframes beat {

    0%,100% {
        transform: rotate(-45deg) scale(1);
    }

    50% {
        transform: rotate(-45deg) scale(1.12);
    }
}


/* =========================
   CHỮ TRONG TIM
========================= */

.heart-text {

    position: absolute;

    z-index: 5;

    color: white;

    font-size: 24px;

    font-weight: bold;

    text-shadow: 0 2px 5px rgba(0,0,0,.15);
}


/* =========================
   LỜI YÊU
========================= */

.love-text {

    font-size: 27px;

    line-height: 1.6;

    color: #b92d67;

    font-weight: 600;
}


.love-text span {

    color: #4f968d;
}


/* =========================
   HOA XUNG QUANH
========================= */

.flower {

    position: fixed;

    z-index: 3;

    pointer-events: none;

    user-select: none;

    animation:
        fall linear infinite;
}


@keyframes fall {

    0% {

        transform:
            translateY(-100px)
            rotate(0deg);

        opacity: 0;
    }

    10% {
        opacity: 1;
    }

    90% {
        opacity: 1;
    }

    100% {

        transform:
            translateY(110vh)
            rotate(360deg);

        opacity: 0;
    }
}


/* =========================
   CÁNH HOA BAY NGANG
========================= */

.petal {

    position: fixed;

    pointer-events: none;

    z-index: 4;

    animation: fly 7s linear infinite;
}


@keyframes fly {

    0% {

        transform:
            translateX(-100px)
            translateY(0)
            rotate(0deg);

        opacity: 0;
    }

    20% {
        opacity: 1;
    }

    80% {
        opacity: 1;
    }

    100% {

        transform:
            translateX(110vw)
            translateY(-150px)
            rotate(500deg);

        opacity: 0;
    }
}


/* =========================
   ĐOM ĐÓM
========================= */

.firefly {

    position: fixed;

    width: 6px;
    height: 6px;

    background: #fff7b2;

    border-radius: 50%;

    box-shadow:
        0 0 8px #fff4a3,
        0 0 20px #fff4a3;

    animation: glow 2s infinite alternate;

    z-index: 5;
}


@keyframes glow {

    from {
        opacity: .2;
        transform: scale(.6);
    }

    to {
        opacity: 1;
        transform: scale(1.4);
    }
}


/* =========================
   HOA GÓC
========================= */

.corner {

    position: fixed;

    font-size: 90px;

    z-index: 6;

    opacity: .9;

    filter:
        drop-shadow(
            0 5px 10px
            rgba(100,100,100,.12)
        );
}


.corner-1 {
    bottom: 10px;
    left: 15px;
}


.corner-2 {
    top: 10px;
    right: 15px;
}


.corner-3 {
    top: 15px;
    left: 20px;
}


.corner-4 {
    bottom: 5px;
    right: 20px;
}


/* =========================
   DÒNG CUỐI
========================= */

.bottom {

    margin-top: 30px;

    color: #668f89;

    font-size: 15px;

    letter-spacing: 1px;
}


</style>
</head>


<body>


<!-- =====================
     HOA GÓC
===================== -->

<div class="corner corner-1">
    🌷🌸
</div>

<div class="corner corner-2">
    🌹🌺
</div>

<div class="corner corner-3">
    🌸🌷
</div>

<div class="corner corner-4">
    🌺🌹
</div>


<!-- =====================
     HOA RƠI
===================== -->

<div class="flower"
style="left:3%; animation-duration:12s;">
🌸
</div>

<div class="flower"
style="left:10%; animation-duration:17s; animation-delay:2s;">
🌷
</div>

<div class="flower"
style="left:18%; animation-duration:14s; animation-delay:5s;">
🌹
</div>

<div class="flower"
style="left:28%; animation-duration:18s; animation-delay:1s;">
🌸
</div>

<div class="flower"
style="left:40%; animation-duration:13s; animation-delay:4s;">
🌺
</div>

<div class="flower"
style="left:52%; animation-duration:16s; animation-delay:3s;">
🌷
</div>

<div class="flower"
style="left:65%; animation-duration:12s; animation-delay:6s;">
🌸
</div>

<div class="flower"
style="left:76%; animation-duration:17s; animation-delay:2s;">
🌹
</div>

<div class="flower"
style="left:88%; animation-duration:14s; animation-delay:5s;">
🌺
</div>

<div class="flower"
style="left:96%; animation-duration:19s;">
🌷
</div>


<!-- =====================
     CÁNH HOA
===================== -->

<div class="petal"
style="top:70%; animation-delay:1s;">
🌸
</div>

<div class="petal"
style="top:40%; animation-delay:3s;">
🌷
</div>

<div class="petal"
style="top:80%; animation-delay:5s;">
🌹
</div>


<!-- =====================
     ĐOM ĐÓM
===================== -->

<div class="firefly" style="left:12%; top:30%;"></div>

<div class="firefly" style="left:22%; top:70%; animation-delay:.5s;"></div>

<div class="firefly" style="left:80%; top:25%; animation-delay:1s;"></div>

<div class="firefly" style="left:90%; top:65%; animation-delay:1.5s;"></div>

<div class="firefly" style="left:70%; top:80%; animation-delay:.8s;"></div>

<div class="firefly" style="left:30%; top:20%; animation-delay:1.2s;"></div>


<!-- =====================
     NỘI DUNG
===================== -->

<div class="page">

    <div class="card">


        <div class="top-flowers">
            🌸 🌷 🌹 🌺 🌷 🌸
        </div>


        <div class="title">
            Yêu Phương Anh
        </div>


        <div class="subtitle">
            Một góc nhỏ dành riêng cho em 🌿
        </div>


        <div class="heart-box">

            <div class="heart"></div>

            <div class="heart-text">
                phuongg anhh
            </div>

        </div>


        <div class="love-text">

            🌸 <span>Phương Anh</span> 🌸

            <br>

            là bông hoa đẹp nhất

            <br>

            trong khu vườn của anh 💗

        </div>


        <div class="bottom">

            🌷 Mong em luôn vui và luôn cười 🌷

        </div>


    </div>

</div>


</body>
</html>
