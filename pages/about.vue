<template>
    <div id="about">
        <div id="heading">
            <h1>about me</h1>
        </div>
        <div id="sections">
        <AboutSection imgurl="images/babyme.jpg" text="I was born in the Bronx to Nigerian immigrants. Growing up, I moved around a bit, living in New York, Illinios, and Texas before high school graduation. As a kid, I wanted to be everything under the sun: a hairdresser, a paramedic, even President." alttext="a baby picture of me" class="left" pos="left" data-aos="fade-right" data-aos-duration="10000" />
        
        <br>

        <AboutSection imgurl="images/collegeme.jpeg" text="I graduated high school and am now attending Columbia University. After a bit of mental debate, I decided on computer science. I've been specifically interested in frontend and web development. " alttext="picture of me with Columbia University sign" class="right" pos="right" data-aos="fade-left" data-aos-duration="10000"/>

        <AboutSection imgurl="images/ibmme.jpeg" text="Through an immersion program with Qubit x Qubit, I interned at IBM in their quantum department. I worked on an open source quantum software benchmarking tool called Red Quuen. I returned back to IBM in summer 2023 as a quantum software developer intern where I worked on a compiler plugin for Qiskit!" alttext="picture of me with IBM hat giving a thumbs up" class="left" pos="left" data-aos="fade-right" data-aos-duration="10000" />

        <AboutSection imgurl="images/jade.jpeg" text="While at Columbia, I've been a part of the JADE program, which is dedicated to helping students learn about the tech and entruprenueship scene in NYC. I've been a participant, instructor, and co-coordinator for the program!" alttext="picture of me with JADE 2024 cohort" class="left" pos="right" data-aos="fade-left" data-aos-duration="10000" />
        </div>
    </div>
</template>

<script>
    import aosMixin from '~/mixins/aos'
    export default {
        mixins: [aosMixin]
    }

</script>

<style>
    @font-face{
        font-family: 'MomcakeBold';
        src: url('../static/fonts/MomcakeBold-WyonA.otf');
    } 

    #about{
        padding: 40px;
    }
    #heading{
        font-size:30px;
        font-family: "MomcakeBold";
        text-align: center;
    }

    #sections{
        display: flex;
        flex-direction: column;
        width: 100%;
    }

    .left{
        width: 70%;
        align-self: flex-start;
        padding-top: 20px;
        padding-bottom: 100px
    }

    .right{
        width: 70%;
        align-self: flex-end;
        padding-top: 20px;
        padding-bottom: 100px
    }

    @media only screen and (max-width: 800px){
        .left, .right{
            width: 100%
        }

    }
</style>