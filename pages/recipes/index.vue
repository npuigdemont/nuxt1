<template>
    <section class="recipes">
        <Recipe 
        v-for="recipe in recipes"
        :key="recipe.id"
        :image="recipe.image"
        :title="recipe.title"
        :previewText="recipe.previewText"
        :id="recipe.id"
        />
      <!-- <Recipe 
        image="https://static01.nyt.com/images/2021/02/17/dining/17tootired-grilled-cheese/17tootired-grilled-cheese-jumbo.jpg?quality=75&auto=webp"
        title="Delicius sandwidch"
        previewText="Widht parma jam"
        id="1"
        />
        <Recipe 
        image="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTSbEeCMLE1_9SJpL-M8DD0ju2kdlebeWGtxA&usqp=CAU"
        title="Omelette"
        previewText="Eggs, potatoes, onions and garlic"
        id="2"
        />--> 
        <article class="recipe">
            <div class="image" style="background-image: url('https://static01.nyt.com/images/2021/02/17/dining/17tootired-grilled-cheese/17tootired-grilled-cheese-jumbo.jpg?quality=75&auto=webp')"></div>
            <h1>title</h1>
            <p>prewiew text</p>
        </article>
        <article class="recipe">
            <div class="image" style="background-image: url('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTSbEeCMLE1_9SJpL-M8DD0ju2kdlebeWGtxA&usqp=CAU')"></div>
            <h1>title</h1>
            <p>prewiew text</p>
        </article>
    </section>
</template>

<script>
import Recipe from '@/components/Recipe'


export default {
    components: {
        Recipe
    },
    asyncData(){
     // return  axios.get('https://swapi.dev/api/vehicles')
     return new Promise ((resolve, reject) => {
         setTimeout(() => {
            resolve({
                recipes: [
                    {
                        id: "1",
                        title: "Delicius sandwidch",
                        previewText: "Widht parma jam",
                        image: "https://static01.nyt.com/images/2021/02/17/dining/17tootired-grilled-cheese/17tootired-grilled-cheese-jumbo.jpg?quality=75&auto=webp"
                    },
                     {
                        id: "2",
                        title: "Omelette",
                        previewText: "Eggs, potatoes, onions and garlic",
                        image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTSbEeCMLE1_9SJpL-M8DD0ju2kdlebeWGtxA&usqp=CAU"
                    }
                ]
            }) 
         }, 1500)
     })
    }
}
</script>

<style scoped>
.recipes {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
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