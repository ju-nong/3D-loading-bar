<template>
    <div class="container">
        <p>{{ status }}</p>
        <div class="progress">
            <div>
                <div></div>
            </div>
            <div>
                <div></div>
            </div>
            <div>
                <div></div>
            </div>
            <div>
                <div></div>
            </div>
            <div>
                <div></div>
            </div>
            <div>
                <div></div>
            </div>
            <div>
                <div></div>
            </div>
            <div>
                <div></div>
            </div>
            <div>
                <div></div>
            </div>
            <div>
                <div></div>
            </div>
            <div>
                <div></div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { onMounted, ref } from "vue";

const status = ref("Loading...");

onMounted(() => {
    setTimeout(() => {
        status.value = "Done!";
    }, 11500);
});
</script>

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

            > div {
                width: 0%;
                height: 100%;
                background-color: #4f78f9;
            }

            &:nth-child(1) {
                width: 250px;
                border-left: 2px solid;

                > div {
                    animation: loading-bar 2.5s linear 0s forwards;
                }
            }

            &:nth-child(2) {
                width: 100px;
                transform: rotateY(90deg) translateZ(-50px) translateX(50px);

                > div {
                    animation: loading-bar 1s linear 2.5s forwards;
                }
            }

            &:nth-child(3) {
                width: 50px;
                transform: translateZ(-100px) translateX(-100px);

                > div {
                    animation: loading-bar 0.5s linear 3.5s forwards;
                }
            }

            &:nth-child(4) {
                width: 100px;
                transform: rotateY(-90deg) translateZ(150px) translateX(-50px);

                > div {
                    animation: loading-bar 1s linear 4s forwards;
                }
            }

            &:nth-child(5) {
                width: 30px;
                transform: translateX(-200px);

                > div {
                    animation: loading-bar 0.3s linear 5s forwards;
                }
            }

            &:nth-child(6) {
                width: 150px;
                transform: translateX(-275px) translateZ(-75px) rotateY(90deg);

                > div {
                    animation: loading-bar 1.5s linear 5.8s forwards;
                }
            }

            &:nth-child(7) {
                width: 20px;
                transform: translateX(-350px) translateZ(-150px);

                > div {
                    animation: loading-bar 0.2s linear 7.3s forwards;
                }
            }

            &:nth-child(8) {
                width: 200px;
                transform: translateX(-450px) translateZ(-50px) rotateY(-90deg);

                > div {
                    animation: loading-bar 2s linear 7.5s forwards;
                }
            }

            &:nth-child(9) {
                width: 100px;
                transform: translateX(-550px) translateZ(50px);

                > div {
                    animation: loading-bar 1s linear 9.5s forwards;
                }
            }

            &:nth-child(10) {
                width: 50px;
                transform: translateX(-575px) translateZ(25px) rotateY(90deg);

                > div {
                    animation: loading-bar 0.5s linear 10.5s forwards;
                }
            }

            &:nth-child(11) {
                width: 50px;
                border-right: 2px solid;
                transform: translateX(-600px);

                > div {
                    animation: loading-bar 0.5s linear 11s forwards;
                }
            }
        }
    }
}
</style>
