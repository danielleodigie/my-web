<template>
    <div :class="pos">
        <img :src="imgurl" :alt="alttext">
        <p>{{text}}</p>
    </div>
</template>

<script>
    export default {
        props: {
            text: String,
            imgurl: String,
            alttext: String,
            pos: String
        }
    }
</script>


<style>
    @font-face{
        font-family: 'ThinLine';
        src: url('../static/fonts/Thin_Line_Font.otf');
    }

    .left, .right {
        display: grid;
        grid-auto-flow: column;
        grid-column-gap: 40px;
        width: 50%;
    }


    .left img, .right img {
        width: 100%;
        max-width: 300px;
        border-radius: 20px;
    }

    .left p, .right p {
        text-align: center;
        margin: auto;
        font-family: "ThinLine";
        font-weight: bold;
        font-size: 25px;
    }

    .right img{
        order: 1;
    }
    @media only screen and (max-width: 800px){

        .left, .right{
            width: 90%;
        }

    }

    @media only screen and (max-width: 480px){

        .left, .right{
            width: 90%;
            display: grid;
            grid-auto-flow: row;
            grid-row-gap: 40px;
            grid-column-gap: 0px;
        }

        .right img{
            order: 0;
        }

    }
</style>