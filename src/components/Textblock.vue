<template>
    <div id="text">
        <h4> Значимость этих проблем настолько очевидна, что консультация с широким активом играет
            важную роль в
            формировании новых предложений. С другой стороны укрепление и развитие структуры обеспечивает
            участие в формировании систем массового участия.
            Разнообразный и богатый опыт консультация с широким активом обеспечивает широкому кругу. Значимость
            этих проблем настолько очевидна, что консультация с широким активом играет важную роль в
            формировании новых предложений.</h4>
    </div>
</template>

<script>
    export default {
        name: "Textblock",
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

    #text {
        h4 {
            margin-top: 20%;
            margin-left: 15%;
            width: 70%;
            font-family: 'Myriad_Pro';
        }
    }


    /*adaptation*/

    @media(min-width:300px) and (max-width:820px) {
        #text {
            h4 {
                width: 80%;
            }
        }
    }

    @media(min-width:768px) and (max-width:1023px) {
        #text {
            h4 {
                width: 90%;
                margin-left: 6%;
            }
        }
    }
</style>