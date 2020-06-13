<template>
    <div id="slider">
        <div class="carousel slide" data-ride="carousel">
            <div class="carousel-inner">
                <div class="carousel-item active">
                    <img src="../assets/bear.png" class="d-block" alt="...">
                </div>
                <div class="carousel-item">
                    <img src="../assets/Camera.png" class="d-block" alt="...">
                </div>
                <div class="carousel-item">
                    <img src="../assets/Devices.png" class="d-block" alt="...">
                </div>
            </div>
            <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="sr-only">Previous</span>
            </a>
            <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                <span class="sr-only">Next</span>
            </a>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Slider',
        data() {
            return {

            }
        }
    }
</script>

<style lang="scss" scoped>
    #slider {

        .slide {
            margin-top: 15%;

            .d-block {
                margin-left: 40%;
                width: 20%;
            }

            .carousel-control-prev {
                .carousel-control-prev-icon {
                    background-color: red;
                }
            }

            .carousel-control-next {
                .carousel-control-next-icon {
                    background-color: red;
                }
            }
        }
    }
</style>