<template>
    <div id="block">
        <div class="col-md-12">
            <form>
                <div class="form-group">
                    <label for="exampleInputEmail1">Оставь телефон и получи что-то офигенное</label>
                    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp"
                        placeholder="Введите номер">
                </div>
                <button type="button" class="btn btn-primary" data-toggle="modal"
                    data-target="#exampleModal">Получить</button>
            </form>
            <!-- Modal -->
            <div class="modal fade" id="exampleModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel"
                aria-hidden="true">
                <div class="modal-dialog" role="document">
                    <div class="modal-content">
                        <div class="modal-header">
                            <h5 class="modal-title" id="exampleModalLabel">Сообщение</h5>
                            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                                <span aria-hidden="true">&times;</span>
                            </button>
                        </div>
                        <div class="modal-body">
                            Ваше сообщение отправленно
                        </div>
                        <div class="modal-footer">
                            <button type="button" class="btn btn-secondary" data-dismiss="modal">Закрыть</button>
                        </div>
                    </div>
                </div>
            </div>
            <!--modal-->
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Formablock',
        data() {
            return {

            }
        }
    }
</script>

<style lang="scss" scoped>
    @font-face {
        font-family: 'Myriad_Pro';
        src: url("../fonts/Myriad_Pro.ttf") format("truetype");
    }

    #block {
        background-image: url('../assets/fon.png');
        background-size: cover;
        width: 100%;
        height: 26rem;
        display: flex;

        .col-md-12 {
            width: 1000px;

            form {
                border: 1px solid black;
                border-radius: 5px 5px 5px 5px;
                width: 20%;
                height: 50%;
                margin-left: 30%;
                margin-top: 7%;
                font-family: 'Myriad_Pro';
                font-size: 150%;
                background: blueviolet;
                color: white;


                input {
                    width: 90%;
                }

                button {
                    margin-left: 10%;
                    width: 80%;
                    background: goldenrod;
                    color: black;
                }

                .form-group {
                    margin-left: 10%;
                }
            }
        }
    }

    /*adaptation*/
    @media (min-width:350px) and (max-width:820px) {
        #block {
            .col-md-12 {
                form {
                    width: 90%;
                    margin-left: 5%;
                    margin-top: 20%;
                }
            }
        }
    }

    @media (min-width:768px) and (max-width:1023px) {
        #block {
            .col-md-12 {
                form {
                    width: 47%;
                    margin-left: 20%;
                    margin-top: 15%;
                }
            }
        }
    }

    @media (min-width:1024px) and (max-width:1370px) {
        #block {
            .col-md-12 {
                form {
                    width: 30%;
                    margin-left: 15%;
                    margin-top: 10%;
                }
            }
        }
    }

    @media (min-width:1920px) {
        #block {
            height: 35rem;

            .col-md-12 {
                form {
                    width: 18%;
                    height: 40%;
                }
            }
        }
    }

    @media (min-width:2500px) {
        #block {
            height: 42rem;
            width: 175rem;

            .col-md-12 {
                form {
                    width: 12%;
                    height: 30%;
                }
            }
        }
    }
</style>