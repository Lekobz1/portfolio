<template>
    <div class="cardBlog">
        <img :src="article.image" :alt="article.title" class="cardBlog__image" />
        <h3 class="cardBlog__title">{{ article.title }}</h3>
        <p class="cardBlog__resume">{{ article.resume }}</p>
        <a :href="article.link" class="cardBlog__readMore">En savoir plus <span class="cardBlog__arrow">&#x2192;</span></a>
    </div>
</template>
  
<script>
export default {
    name: "CardBlog",
    props: {
        article: {
            //typage puis requis
            type: Object,
            required: true,
        },
    },
};
</script>