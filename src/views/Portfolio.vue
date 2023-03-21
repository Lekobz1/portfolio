<template>

<div class="presentation">
    <div>
        <h2>developpement web</h2>
        <img class="img" src="../assets/prestations.jpg" alt="presta">
    </div>
    <div>
        <h2>Photo</h2>
        <img class="img" src="../assets/prestations.jpg" alt="presta">
    </div>
    <div>
        <h2>Video</h2>
        <img class="img" src="../assets/prestations.jpg" alt="presta">
    </div> 
</div>
    
</template>

<style>

.presentation{
    display: flex;
    height: 10rem;
    gap: 1rem;
}

.presentation > div {
    flex: 1;
    border-radius: 1rem;
    background-position: center;
    background-repeat: no-repeat;
    background-size: auto 100%;
    transition: all .8s cubic-bezier(.25, .4, .45, 1.4);
}

.presentation > div:hover{
    flex: 5;
}

.img{
    width: 500px;
    height: 500px;
    object-fit: contain;
}

</style>