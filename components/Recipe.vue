<template>
<div>
    <nuxt-link :to="'/recipes/' + id">
        <article class="recipe">
            <div class="image" :style="{backgroundImage: 'url(' + image + ')'}"></div>
            <h1>{{title}}</h1>
            <p>{{previewText}}</p>
        </article>
    </nuxt-link>
    
        </div>
</template>
<script>
export default {
    props: ['image', 'title', 'previewText', 'id']
}
</script>

<style scoped>
a {
  text-decoration: none;
  color: black;  
}
.recipe {
    box-sizing: border-box;
    width: 280px;
    padding: 8px;
    border: 1px solid #ccc;
    margin: 8px;
}
.image {
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 200px;
}
</style>