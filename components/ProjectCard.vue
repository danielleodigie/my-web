<template>
    <div>
        <a :href="pagelink" target="_blank">
            <div id="projectcard">
                <img :src="imgurl" :alt="alttext" />
                <h3>{{title}}</h3>
                <p>{{languages}}</p>
            </div>
        </a>
    </div>
</template>

<script>
     export default {
        props: {
            title: String,
            imgurl: String,
            alttext: String,
            languages: String,
            pagelink: String
        }
    }

</script>

<style>
    a{
        text-decoration: none;
        color: black;
    }
    #projectcard{
        margin: auto;
        transition: 400ms;
        display: grid;
        grid-auto-flow: row;
        border: 1px solid grey;
        border-radius: 15px;
        width: 90%;
        max-width: 425px;
        
    }
    
    #projectcard img{
        width: 100%;
        height:auto;
        border-bottom: 1px solid grey;
        border-radius: 15px 15px 0px 0px;
    }

    #projectcard h3{
        padding: 10px;
        font-family: "MomcakeBold";
        font-size: 25px;
        text-decoration: none;
    }

    #projectcard p{
        font-size: 18px;
        font-family: "ThinLine";
        padding: 10px;
        padding-bottom: 0px;
        text-decoration: none;
    }

    #projectcard:hover, #projectcard:active{
        transition: 400ms;
        box-shadow: 0 0 25px #394d35;
    }
</style>
