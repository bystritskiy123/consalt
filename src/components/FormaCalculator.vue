<template>
    <div id="main">
        <div id="Calculator">
            <div id="gallery">
                <label v-for="img in $options.imgNames" :key="img">
                    <input type="radio" :value="img" v-model="selectedimg">
                    {{img}}
                </label>
            </div>
        </div>
        <div id="forma" class="conatiner-fluid">
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
    </div>
</template>

<script>
    export default {
        name: 'FormaCalculator',
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
                return require(`../assets/img/${fileName}.png`);
            }
        },
        // A small trick to have non-reactive elements in the component.
        imgNames: ["1", "2", "3", "4", "5"]
    }
</script>

<style lang="scss" scoped>
    @font-face {
        font-family: 'Myriad_Pro';
        src: url("../fonts/Myriad_Pro.ttf") format("truetype");
    }

    #main {
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
            height: 45rem;
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
                            width: 40%;
                            margin-left: 5%;
                        }

                        h4 {
                            margin-left: 30%;
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
                    margin-top: 16%;
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
                    margin-top: 15%;
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
                    margin-top: 16%;
                }

                .form-control {
                    width: 40%;
                }
            }

            .two {
                margin-top: 19%;
                font-family: 'Myriad_Pro';
                font-size: 130%;
                width: 30%;
                border-radius: 4px 4px 4px 4px;
                background: rebeccapurple;
                color: white;
            }
        }
    }

    /*adaptation*/
    @media (min-width:300px) and (max-width:820px) {
        #main {
            #forma {
                height: 40rem;

                #part_1 {
                    form {
                        #page {
                            h4 {
                                display: none;
                            }

                            label {
                                h4 {
                                    display: none;
                                }
                            }

                            img {
                                width: 100%;
                                margin-top: 20%;
                            }
                        }

                        #label {
                            margin-left: 10%;

                            label {
                                font-size: 130%;
                            }
                        }

                        #input {
                            width: 100%;
                            margin-left: 5%;
                        }
                    }

                    .one {
                        width: 100%;
                        margin-left: 0%;
                        margin-top: 110%;
                        font-size: 110%;
                    }
                }

                #part_2 {
                    h4 {
                        font-size: 100%;
                        margin-top: 20%;
                    }

                    h5 {
                        font-size: 120%;
                        margin-top: 20%;
                    }

                    #radio {
                        font-size: 90%;
                    }

                    #inputState {
                        width: 100%;
                    }

                    .two {
                        width: 100%;
                        font-size: 110%;
                        margin-top: 100%;
                    }
                }
            }
        }
    }

    @media (min-width:768px) and (max-width:1023px) {
        #main {
            #forma {
                height: 40rem;

                #part_1 {
                    form {
                        #page {
                            margin-left: 0%;

                            h4 {
                                display: flex;
                                margin-left: 40%;
                            }

                            label {
                                h4 {
                                    display: flex;
                                }
                            }

                            img {
                                width: 50%;
                                margin-top: 5%;
                            }
                        }

                        #label {
                            margin-left: 15%;
                            margin-top: 20%;

                            label {
                                font-size: 130%;
                            }
                        }

                        #input {
                            width: 80%;
                            margin-left: 13%;
                        }
                    }

                    .one {
                        width: 50%;
                        margin-left: 30%;
                        margin-top: 30%;
                        font-size: 110%;
                    }
                }

                #part_2 {
                    h4 {
                        font-size: 100%;
                    }

                    h5 {
                        font-size: 120%;
                    }

                    #radio {
                        font-size: 90%;
                    }

                    h6 {
                        margin-top: 25%;
                    }

                    #inputState {
                        width: 100%;
                    }

                    .two {
                        width: 50%;
                        font-size: 110%;
                        margin-top: 35%;
                    }
                }
            }
        }
    }

    @media (min-width:1024px) and (max-width:1370px) {
        #main {
            #forma {
                #part_1 {
                    .one {
                        width: 40%;
                        margin-top: 18%;
                    }

                    form {
                        #label {
                            margin-top: 10%;
                        }

                        #input {
                            margin-left: 25%;
                            width: 60%;
                        }
                    }
                }

                #part_2 {
                    h6 {
                        margin-top: 20%;
                    }

                    .two {
                        margin-top: 22%;
                    }
                }
            }
        }
    }


    @media (min-width:1920px) {
        #main {
            #forma {
                height: 65rem;

                #part_1 {
                    form {
                        #label {
                            margin-top: 10%;
                            margin-left: 25%;
                        }
                    }

                    .one {
                        margin-top: 20%;
                    }
                }

                #part_2 {
                    h6 {
                        margin-top: 26%;
                    }

                    .two {
                        margin-top: 22%;
                    }
                }
            }
        }
    }


    @media (min-width:2500px) {
        #main {
            #forma {
                height: 80rem;

                #part_1 {
                    form {
                        #page {
                            h4 {
                                font-size: 300%;
                            }
                        }

                        #label {
                            margin-left: 25%;
                            font-size: 150%;
                        }

                        #input {
                            margin-left: 28%;

                            input {
                                width: 35%;
                                height: 3rem;
                            }
                        }
                    }
                }


                #part_2 {
                    h4 {
                        font-size: 300%;
                    }

                    h5 {
                        font-size: 300%;
                    }

                    #radio {
                        p {
                            font-size: 250%;
                        }
                    }

                    h6 {
                        font-size: 250%;
                        margin-top: 22%;
                    }

                    .two {
                        margin-top: 22%;
                    }
                }
            }
        }
    }
</style>