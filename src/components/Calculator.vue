<template>
    <div id="main" class="container-fluid">
        <div id="card" class="row">
            <div class="card border-0" style="width: 11rem;">
                <img src="../assets/img_1.png" class="card-img-top" alt="...">
                <div class="card-body">
                    <p class="card-text">
                        Одностворчатое
                    </p>
                </div>
            </div>

            <div class="card border-0" style="width: 15rem;">
                <img src="../assets/img_2.png" class="card-img-top" alt="...">
                <div class="card-body">
                    <p class="card-text">двухстворчатые</p>
                </div>
            </div>

            <div class="card border-0" style="width: 15rem;">
                <img src="../assets/img_3.png" class="card-img-top" alt="...">
                <div class="card-body">
                    <p class="card-text">Трёстворчатые</p>
                </div>
            </div>

            <div class="card border-0" style="width: 15rem;">
                <img src="../assets/img_4.png" class="card-img-top" alt="...">
                <div class="card-body">
                    <p class="card-text">Балконный блок</p>
                </div>
            </div>

            <div class="card border-0" style="width: 15rem;">
                <img src="../assets/img_5.png" class="card-img-top" alt="...">
                <div class="card-body">
                    <p class="card-text">остекление балкона</p>
                </div>
            </div>
        </div>

        <!--Calculator-->
        <FormaCalculator />
        <!--Calculator-->
    </div>
</template>


<script>
    import FormaCalculator from './FormaCalculator.vue'
    export default {
        name: 'Calculator',
        data() {
            return {

            }
        },
        components: {
            FormaCalculator,
        }
    }
</script>


<style lang="scss" scoped>
    @font-face {
        font-family: 'Myriad_Pro';
        src: url("../fonts/Myriad_Pro.ttf") format("truetype");
    }

    #main {

        #card {
            margin-top: 10%;
            margin-left: 5%;

            .card {
                margin-left: 3%;
                font-family: 'Myriad_Pro';
                font-size: 110%;
            }
        }


    }


    @media (min-width:300px) and (max-width:820px) {
        #main {
            #card {
                margin-top: 30%;

                .card {
                    margin-left: 10%;
                }
            }
        }
    }

    @media (min-width:1024px) and (max-width:1370px) {
        #main {
            #card {
                margin-left: 10%;
            }
        }
    }

    @media (min-width:1920px) {
        #main {
            #card {
                margin-left: 12%;
            }
        }
    }
</style>