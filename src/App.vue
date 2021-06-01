<template>
<div>
    <section>
        <nav>
            <div class="left">
                <ul>
                    <li id="home"><i class="fa fa-home"></i> Home</li>
                    <li id="home"><i class="fa fa-home"></i> Home</li>
                    <li id="home"><i class="fa fa-home"></i> Home</li>
                    <li id="home"><i class="fa fa-home"></i> Home</li>
                </ul>
            </div>
        </nav>

        <div class="container">
            <div class="title">
                <h1><span class="black">KURDESTAN</span> <span class="outlined">TOURISM</span></h1>
            </div>

            <div class="forest">
                <img src="./assets/img/f-dark.png" class="f-dark">
                <img src="./assets/img/11.png" alt="Forest">

            </div>

            <div class="desc">
                <h3 class="sub-title">A magnificent stair-stepped village in the beautiful Kurdistan</h3>
            </div>

            <div>
                <img src="./assets/img/cloud1.png" class="cloud1">
                <img src="./assets/img/cloud2.png" class="cloud2">
                <img src="./assets/img/cloud3.png" class="cloud3">
                <img src="./assets/img/cloud1.png" class="cloud4">
                <img src="./assets/img/cloud2.png" class="cloud5">
                <img src="./assets/img/cloud3.png" class="cloud6">
            </div>

            <div class="bg-image">
                <div class="bg-dark">
                </div>
            </div>
        </div>
    </section>
</div>
</template>

<script>
import gsap from 'gsap'
export default {
    name: 'App',
    mounted() {
        gsap.from('.title', 8.5, {
            y: 1000,
        })
        gsap.from('.bg-image', 3, {
            opacity: 0,
            y: 0,
        })
        gsap.from('.forest', 3, {
            opacity: 0,
            y: 200,
        })
        gsap.from('nav', 1, {
            y: 30,
            autoAlpha: 0,
        }, '-=1')
        gsap.from('.sub-title', 4, {
            x: -500,
            autoAlpha: 0,
        })
        gsap.from('.bottom-nav', 2, {
            width: '0%',
            autoAlpha: 0,
        }, '-=2');
    },
    methods: {
        beforeEnter() {
            // gsap.from(el, {
            //     y: 0,
            //     scale: 1,
            //     ease: 'easeInOut'
            // })

        },
        enter() {
            gsap.set('.grid', {
                display: 'grid'
            })
            gsap.to('.forest img', 3, {
                y: -400,
                scale: 1.1,
            })
            gsap.to('.bg-image', 3, {
                y: -600,
            }, '-=3')
            gsap.to('.sub-title', 3, {
                autoAlpha: 0,
                y: -100,
            }, '-=3')
            gsap.to('.bottom-nav', 3, {
                width: '0%',
            }, '-=3')
            gsap.to('nav', 3, {
                color: '#fff',
            }, '-=3')
            gsap.to('.imgs', 2, {
                height: '100%',
            }, '-=2')
            gsap.to('.imgs-2', 2, {
                height: '100%',
            }, '-=1.8')
            gsap.to('.imgs-3', 2, {
                height: '100%',
            }, '-=1.7')
            gsap.to('.imgs-4', 2, {
                height: '100%',
            }, '-=1.6')
            gsap.to('.destination', 2, {
                autoAlpha: 1,
                y: -20,
            }, '-=1.6');

        },
        show() {
            this.visiable = !this.visiable
        }
    }

}
</script>

<style>
#app {
    font-family: Avenir, Honevetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;

}

body {
    overflow-x: hidden;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

section {
    height: 100vh;
    width: 100%;
    overflow: hidden;
}

nav {
    position: fixed;
    width: 100%;
    top: 20px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    font-family: 'Poppins', sans-serif;
    font-weight: bolder;
    color: #232123;
    z-index: 9999999;
}

.middle {
    font-family: 'Oswald', sans-serif;
    text-align: center;
    padding-top: 10px;
    padding-bottom: 10px;
    letter-spacing: 1px;
}

ul {
    list-style: none;
}

li {
    display: inline;
    margin-right: 20px;
    margin-left: 20px;
    cursor: pointer;
    z-index: 999;
}

.container {
    position: roneative;
    height: 100%;
    width: 100%;
}

.title {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    position: fixed;
    z-index: -1;
    font-family: 'Oswald', sans-serif;
    font-size: 80px;
    letter-spacing: 1px;
    margin-top: -67px !important;
    transform: scaleY(1.7);
}

.black {
    color: #232123;

}

.outlined {
    color: transparent;
    -webkit-text-stroke: 2px #232123;
    opacity: 0.8;
}

.desc {
    position: fixed;
    bottom: 0;
    height: 250px;
    width: 55%;
    display: flex;
    flex-direction: row;
    align-items: flex-start;
}

.sub-title {
    color: white;
    font-family: 'Poppins', sans-serif;
    padding-bottom: 25px;
    width: 65%;
    overflow: hidden;
    align-self: flex-end;
}

.bottom-nav {
    width: 100%;
    height: 80px;
    background: #CAC5C1;
    display: flex;
    align-items: center;
    justify-content: flex-end;
}

.bottom-nav h4 {
    font-family: 'Oswald', sans-serif;
    transform: scaleY(1.7) translateX(-20px);
    color: #232123;
    transition: .7s all;
}

.circle {
    width: 20px;
    height: 20px;
    border-radius: 50%;
    border: 1px solid #232123;
    margin: 0 20px;
    cursor: pointer;
}

.circle::before {
    content: '';
    display: block;
    height: 1.5px;
    width: 15px;
    background-color: #232123;
    margin-top: 46%;
    margin-left: -50%;
}

.circle::after {
    content: '';
    display: block;
    height: 50px;
    width: 50px;
    border-radius: 50%;
    opacity: 0.2;
    background-color: #232123;
    margin-left: -200px;
    margin-top: -130%;
    transition: .7s all;
    transition-timing-function: ease;

}

.bottom-nav:hover .circle::after {
    transition: .7s all;
    transition-timing-function: ease;
    margin-left: -15px;
}

.bottom-nav:hover h4 {
    transform: scaleY(1.7) translateX(0px);
}

.forest {
    position: fixed;
    top: 50vh;
    width: 100%;
    height: 100%;
    z-index: -1;
}

.forest img {
    width: 100%;
}

.grid {
    display: none;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: repeat(12, 1fr);
    grid-column: 1/span 12;
    grid-row: 1/span 12;
    width: 100%;
    height: 100%;
    grid-row-gap: 2px;
    grid-column-gap: 2px;
    position: absolute;
    top: 0;
}

.imgs {
    grid-column: 3/span 4;
    grid-row: 3/span 8;
    width: 100%;
    height: 0%;
    overflow: hidden;
    position: roneative;
    top: 100%;
    transform-origin: top;
    transform: rotateX(180deg);
}

.img-wrapper {
    position: absolute;
    top: 0;
    width: 100%;
    transform: rotateX(180deg);
    cursor: pointer;
    transition: .7s all;
}

.img-wrapper:hover {
    transform: rotateX(180deg) scale(1.1);
}

.first-img {
    height: 600px;
    background: url("./assets/img/first.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
}

.imgs-2 {
    grid-column: 7/span 2;
    width: 100%;
    grid-row: 3/span 5;
    width: 100%;
    height: 0%;
    overflow: hidden;
    position: roneative;
    top: 100%;
    transform-origin: top;
    transform: rotateX(180deg);
}
.left ul li{
    display: flex;
    justify-content: flex-end;
    direction: ltr;
    float: left;
    z-index: 99999999999 ;
}
.second-img {
    height: 400px;
    background: url("./assets/img/second.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
}

.imgs-3 {
    grid-column: 7/span 2;
    width: 100%;
    grid-row: 8/span 3;
    width: 100%;
    height: 0%;
    overflow: hidden;
    position: roneative;
    top: 100%;
    transform-origin: top;
    transform: rotateX(180deg);
}

.third-img {
    height: 300px;
    background: url("./assets/img/third.png");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}

.imgs-4 {
    grid-column: 9/span 2;
    width: 100%;
    grid-row: 3/span 8;
    width: 100%;
    height: 0%;
    overflow: hidden;
    position: roneative;
    top: 100%;
    transform-origin: top;
    transform: rotateX(180deg);
}

.forth-img {
    height: 600px;
    background: url("./assets/img/forth.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
}

.destination {
    grid-column: 2/span 2;
    grid-row: 10/span 1;
    z-index: 1;
    font-family: 'Oswald', sans-serif;
    font-size: 30px;
    color: white;
    letter-spacing: 1px;
    transform: scaleY(1.5) translateY(20px);
    margin: 0;
    padding: 0;
    opacity: 0;
}

.white_outline {
    -webkit-text-stroke: 1px #fff;
}

.bg-dark {
    background: #000;
    width: 100%;
    height: 3500px;
    position: absolute;
    animation: op2 8s forwards;

}

.bg-image {
    width: 100%;
    height: 100%;
    top: 0;
    z-index: -2;
    position: fixed;
    background: url("./assets/img/sky23.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center bottom;

}

.cloud1 {
    position: absolute;
    top: 0;
    left: 0;
    max-width: 500px;
    z-index: 10000;
    animation: animateCloud 50s linear infinite;
}

.cloud2 {
    position: absolute;
    top: 0;
    left: 0;
    max-width: 400px;
    z-index: 10000;
    animation: animateCloud 35s linear infinite;
}

.cloud3 {
    position: absolute;
    top: 0;
    left: 0;
    max-width: 400px;
    z-index: 10000;
    animation: animateCloud 80s linear infinite;

}

.cloud4 {
    position: absolute;
    top: 200px;
    left: 0;
    max-width: 200px;
    z-index: 10000;
    animation: animateCloud 70s linear infinite;
    animation-delay: -20s;
}

.cloud5 {
    position: absolute;
    top: 150px;
    left: 0;
    max-width: 400px;
    z-index: 10000;
    animation: animateCloud 40s linear infinite;
    animation-delay: -5s;
}

.cloud6 {
    position: absolute;
    top: 75px;
    left: 0;
    max-width: 300px;
    z-index: 10000;
    animation: animateCloud 30s linear infinite;
    animation-delay: -10s;
}

.f-dark {
    position: fixed;
    top: 48vh;
    width: 100%;
    height: 100%;
    top: 392px;
    animation: op2 8s forwards;
}

@keyframes animateCloud {
    0% {
        transform: translateX(-100%) scale(1);
    }

    100% {
        transform: translateX(400%) scale(1.5);
    }
}

@keyframes op {
    0% {
        opacity: 0.9;
    }

    30% {
        opacity: 0.7;
    }

    50% {
        opacity: 0.5;
    }

    70% {
        opacity: 0.3;
    }

    100% {
        opacity: 0.1;
    }
}

@keyframes op2 {
    0% {
        opacity: 0.5;
    }

    30% {
        opacity: 0.3;
    }

    50% {
        opacity: 0.2;
    }

    70% {
        opacity: 0.1;
    }

    100% {
        opacity: 0.1;
    }
}

@media only screen and (max-width: 1175px) {
    .title {
        font-size: 60px;
    }

    .sub-title {
        width: 90%;
    }
}

@media only screen and (max-width: 887px) {
    .title {
        font-size: 50px;
    }

    .sub-title {
        width: 90%;
        font-size: 15px;
    }

    .imgs {
        grid-row: 3/span 6;
    }

    .first-img {
        height: 400px;
    }

    .imgs-2 {
        grid-row: 9/span 2;
        grid-column: 3/span 4;
    }

    .imgs-3 {
        grid-row: 3/span 3;
        grid-column: 7/ span 4;
    }

    .third-img {
        height: 200px;
    }

    .imgs-4 {
        grid-row: 6/span 5;
        grid-column: 7/ span 4;
    }

}

@media only screen and (max-width: 762px) {
    .title {
        font-size: 30px;
    }

    .sub-title {
        width: 90%;
        font-size: 12px;
    }

    .bottom-nav {
        height: 60px;
        font-size: 15px;
    }

    .forest img {
        height: 100%;
        width: 130%;
        margin-left: -15%;
    }

    nav {
        flex-direction: column;
        font-size: 13px;
    }
}
</style>
