<template>
    <div class="container">
        <p>Loading...</p>
        <div class="progress">
            <div></div>
            <div></div>
            <div></div>
            <div></div>
            <div></div>
            <div></div>
            <div></div>
            <div></div>
            <div></div>
            <div></div>
            <div></div>
        </div>
    </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    row-gap: 10px;
    transition: all 0.3s;
    transform: translateX(325px);
    transform-style: preserve-3d;

    &:hover {
        transform: rotateX(-25deg) rotateY(-25deg) translateX(325px);
    }

    p {
        font-size: 18px;
        font-weight: 600;
    }

    .progress {
        width: 1100px;
        height: 50px;
        display: flex;
        transform-style: preserve-3d;

        > div {
            background-color: #fff;
            border-color: #000;
            height: 100%;
            border-top: 2px solid;
            border-bottom: 2px solid;

            &:nth-child(1) {
                width: 250px;
                border-left: 2px solid;
            }

            &:nth-child(2) {
                width: 100px;
                transform: rotateY(90deg) translateZ(-50px) translateX(50px);
            }

            &:nth-child(3) {
                width: 50px;
                transform: translateZ(-100px) translateX(-100px);
            }

            &:nth-child(4) {
                width: 100px;
                transform: rotateY(-90deg) translateZ(150px) translateX(-50px);
            }

            &:nth-child(5) {
                width: 30px;
                transform: translateX(-200px);
            }

            &:nth-child(6) {
                width: 150px;
                transform: translateX(-275px) translateZ(-75px) rotateY(90deg);
            }

            &:nth-child(7) {
                width: 20px;
                transform: translateX(-350px) translateZ(-150px);
            }

            &:nth-child(8) {
                width: 200px;
                transform: translateX(-450px) translateZ(-50px) rotateY(-90deg);
            }

            &:nth-child(9) {
                width: 100px;
                transform: translateX(-550px) translateZ(50px);
            }

            &:nth-child(10) {
                width: 50px;
                transform: translateX(-575px) translateZ(25px) rotateY(90deg);
            }

            &:nth-child(11) {
                width: 50px;
                border-right: 2px solid;
                transform: translateX(-600px);
            }
        }
    }
}
</style>
