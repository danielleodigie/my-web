<template>
    <div class="navbar">
        <NuxtLink to="/" id="home">danielle.</NuxtLink>
        <ul id="navlinks">
            <NuxtLink to="/about">About</NuxtLink>
            <NuxtLink to="/projects">Projects</NuxtLink>
        </ul>
        <hr>
    </div>
</template>

<script>
</script>

<style>
    @font-face{
        font-family: 'TypoGraphica';
        src: url('../static/fonts/Typographica-Blp5.ttf');
    }
    @font-face{
        font-family: 'ThinLine';
        src: url('../static/fonts/Thin_Line_Font.otf');
    }

    @font-face{
        font-family: 'MomcakeBold';
        src: url('../static/fonts/MomcakeBold-WyonA.otf');
    }
    #navlinks {
        display: flex;
        list-style: none;
        float: right;
        margin: 0;
        padding: 25px;
        

    }
    #home {
        float: left;
        text-decoration: none;
        font-family: 'TypoGraphica';
        font-size: 50px;
        margin-left: 18px;
        margin-top: 4px;
        color: #061507;
    }

    #home a:visited{
        color: #061507;
    }

    #navlinks a{
        text-decoration: none;
        color: #061507;
        font-size: 25px;
        padding-right: 20px;
        font-family: 'ThinLine';
        font-weight: 900;
    }

    hr{
        width: 100%;
        height: 3px;
        background-color: #5C7457;
        border-radius: 3px;
    }
    
    @media only screen and (max-width: 480px){
        #home{
            font-size: 30px;
            margin-top: 15px;
        }

        #navlinks a{
            font-size: 20px;
        }
    }
</style>