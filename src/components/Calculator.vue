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
                <label v-for="img in $options.imgNames" :key="img">
                    <input type="radio" :value="img" v-model="selectedimg">
                    {{img}}
                </label>
            </div>
            <!--<img :src="imgImage" :alt="selectedimg">-->
        </div>
        <div id="forma">
            <div class="col-md-6" id="part_1">
                <form>
                    <div class="form-group" id="page">
                        <h4>Ширина</h4>
                        <label for="exampleInputEmail1">
                            <h4>Высота</h4>
                        </label>
                        <img :src="imgImage" :alt="selectedimg">
                    </div>
                    <div class="row" id="label">
                        <label for="exampleInputEmail1">Ширина,см</label>
                        <label for="exampleInputEmail1">высота,см</label>
                    </div>
                    <div class="form-group" id="input">
                        <input type="text" class="form-control" id="exampleInputPassword1">
                        <h5>X</h5>
                        <input type="text" class="form-control" id="exampleInputPassword1">
                    </div>
                </form>
                <button type="button" class="one">Введите номер</button>
            </div>
            <form class="col-md-6" id="part_2">
                <h4>Одностворчатое окно KBE</h4>
                <h5>1.Критерий выбора</h5>
                <div class="row" id="radio">
                    <p><input name="punkt" type="radio" value="punkt">Пункт выбора 1</p>
                    <p><input name="punkt" type="radio" value="punkt">Пункт выбора 2</p>
                    <p><input name="punkt" type="radio" value="punkt">Пункт выбора 3</p>
                </div>
                <h6>2.Выбирите открывание створки</h6>
                <select id="inputState" class="form-control">
                    <option value="left">Влево</option>
                    <option value="right">Вправо</option>
                </select>
                <button type="button" class="two">Расчитать</button>
            </form>
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
        }

        #forma {
            height: 40rem;
            display: flex;
            margin-top: 15%;
            border: 3px solid black;
            border-radius: 5px 5px 5px 5px;

            #part_1 {
                form {
                    margin-top: 5%;

                    #page {
                        margin-left: 10%;

                        img {
                            width: 50%;
                            margin-left: 5%;
                        }

                        h4 {
                            margin-left: 35%;
                        }

                        label {
                            h4 {
                                transform: rotate(-90deg);
                                transform-origin: left top 2;
                            }
                        }
                    }
                }

                #input {
                    display: flex;
                    margin-left: 20%;
                    width: 50%;
                }

                #label {
                    margin-left: 22%;

                    label {
                        margin-left: 5%;
                        font-size: 150%;
                    }
                }

                .one {
                    margin-left: 50%;
                    margin-top: 40%;
                    font-family: 'Myriad_Pro';
                    font-size: 130%;
                    width: 30%;
                    border-radius: 4px 4px 4px 4px;
                }
            }

            #part_2 {
                h4 {
                    font-family: 'Myriad_Pro';
                    color: blue;
                    margin-top: 10%;
                }

                h5 {
                    font-family: 'Myriad_Pro';
                    margin-top: 10%;
                    font-size: 150%;
                }

                #radio {
                    margin-top: 3%;

                    p {
                        margin-left: 2%;
                        font-family: 'Myriad_Pro';
                        font-size: 120%;
                    }
                }

                h6 {
                    font-family: 'Myriad_Pro';
                    font-size: 130%;
                    margin-top: 15%;
                }

                .form-control {
                    width: 40%;
                }
            }

            .two {
                margin-top: 10%;
                font-family: 'Myriad_Pro';
                font-size: 130%;
                width: 30%;
                border-radius: 4px 4px 4px 4px;
                background: rebeccapurple;
                color: white;
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