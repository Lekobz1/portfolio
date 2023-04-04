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

<script>

export default {

    name : 'MenuPortfolio'
}

</script>

<style scoped>

.presentation{
    display: flex;
    height: 10rem;
    gap: 1rem;
}
.img{
    width: 500px;
    height: 500px;
    object-fit: contain;
}

</style>