<template>
    <div id="footer">
        <div id="content">
            <h2>Футер</h2>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Lastblock',
        data() {
            return {

            }
        }
    }
</script>

<style lang="scss" scoped>
    #footer {
        width: 100%;
        height: 10rem;
        background-color: gray;
        background-size: cover;
        margin-top: 10%;
        display: flex;

        #content {
            width: 1000px;
            display: flex;

            h2 {
                margin-left: 70%;
                margin-top: 6%;
            }
        }
    }

    @media (min-width:300px) and (max-width:820px) {
        #footer {
            #content {
                h2 {
                    margin-left: 40%;
                    margin-top: 15%;
                }
            }
        }
    }

    @media (min-width:768px) and (max-width:1023px) {
        #footer {
            #content {
                h2 {
                    margin-top: 7%;
                    margin-left: 45%;
                }
            }
        }
    }

    @media (min-width:1024px) and (max-width:1370px) {
        #footer {
            #content {
                h2 {
                    margin-left: 47%;
                }
            }
        }
    }

    @media (min-width:1920px) {
        #footer {
            #content {
                h2 {
                    margin-left: 90%;
                }
            }
        }
    }

    @media (min-width:2500px) {
        #footer {
            #content {
                h2 {
                    margin-left: 120%;
                }
            }
        }
    }
</style>