<template>
<footer class="container">
    
        <div class="logo">
            <img class="imglogo" src="../assets/logo site.svg" alt="Logo Jonathan Simon">
        </div>
        <div class="cta">
            <p class="calltoaction">je souhaite realiser un projet !</p>
        </div>
</footer>

</template>

<style scoped>
.container { 
    width: 100vw;
    background-color: rgba(249, 244, 237, 1);
    display: grid;
    grid-template-columns: 20% 60% 20%;
    grid-template-rows: 100%;
    gap: 0% 0%;
    grid-auto-flow: row;
    grid-template-areas: "logo cta copie";
    
    
}

.logo { 
    grid-area: logo; 
}

.cta { 
    grid-area: cta; 
}

.copie { 
    grid-area: copie; 
}

.calltoaction{
box-shadow: 0px 6px 4px rgba(0, 0, 0, 0.25);
font-family: 'PT Serif';
font-style: normal;
font-weight: 700;
font-size: 24px;
line-height: 31px;
color: #C58940;
}

.imglogo{
width: 150px;
height: 150px;
}

</style>