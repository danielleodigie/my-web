<template>
    <div id="projects">
        <div id="heading">
            <h1>Projects</h1>
        </div>
        <div id="cards">
        <ProjectCard title="Red Queen" imgurl="images/redqueen2.jpg" alttext="chess board" languages="Qiskit, QASM" pagelink="#" />

        <ProjectCard title="MelaHealth" imgurl="images/melahealth.png" alttext="sample image" languages="Flask, HTML, CSS" pagelink="#" />
        </div>
    </div>
</template>

<style>

    #projects {
        padding: 40px;
        margin: auto;
        
    }

    #cards{
        margin: auto;
        padding: 40px;
        display: grid;
        grid-auto-rows: auto;
        grid-gap: 2em;
        grid-template-columns: repeat(2, 1fr);
    }

    @media only screen and (max-width: 800px){
        #cards{
            padding: 0;
            grid-template-columns: repeat(1, 1fr);
        }

    }
</style>