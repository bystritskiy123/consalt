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
</style>