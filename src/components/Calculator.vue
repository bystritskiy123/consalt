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
        <div id="Calculator">
            <div id="gallery">
                <label v-for="img in $options.imgNames" :key="img" style="margin-right: 2rem">
                    <input type="radio" :value="img" v-model="selectedimg">
                    {{img}}
                </label>
            </div>
            <img :src="imgImage" :alt="selectedimg">
        </div>
        <!--Calculator-->
    </div>
</template>


<script>
    export default {
        name: 'Calculator',
        data() {
            return {
                selectedimg: ""
            }
        },
        computed: {
            imgImage() {
                // Return nothing for the default empty string
                if (!this.selectedimg) {
                    return;
                }

                const fileName = this.selectedimg.toLowerCase();

                // Request the image as a webpack module by using `require`
                return require(`../assets/${fileName}.png`);
            }
        },
        // A small trick to have non-reactive elements in the component.
        imgNames: ["img_1", "img_2", "img_3", "img_4", "img_5"]
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

        #Calculator {
            #gallery {
                display: flex;
                justify-content: space-around;
                align-items: center;
                width: 100%;
                margin-left: 1%;
            }

            img {
                margin-left: 10%;
                margin-top: 10%;
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