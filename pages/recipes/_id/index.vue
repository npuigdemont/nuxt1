<template>
    <section class="single-recipe">
        <h1> {{ recipe.title }}</h1>
        <div>
            <img :src="recipe.image" :alt="recipe.title">
        </div>
        <h3>{{recipe.previewText}}</h3>
        <p>{{ recipe.descriptionText }}</p>
    </section>
</template>

<script>
export default {
   asyncData(context){
     // return  axios.get('https://swapi.dev/api/vehicles')
     return new Promise ((resolve, reject) => {
         setTimeout(() => {
            resolve({
                recipe: [
                    {
                        id: "1",
                        title: "Delicius sandwidch",
                        previewText: "Widht parma jam",
                        descriptionText: "this is the description text for the sandwidch",
                        image: "https://static01.nyt.com/images/2021/02/17/dining/17tootired-grilled-cheese/17tootired-grilled-cheese-jumbo.jpg?quality=75&auto=webp"
                    },
                     {
                        id: "2",
                        title: "Omelette",
                        previewText: "Eggs, potatoes, onions and garlic",
                        descriptionText: "this is the description text for the omelette",
                        image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTSbEeCMLE1_9SJpL-M8DD0ju2kdlebeWGtxA&usqp=CAU"
                    }
                ].find(el => el.id === context.params.id)
            }) 
         }, 1500)
     })
    }
}
</script>

<style scoped>
.single-recipe {
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 30px;
}
img {
    width: 75%;
}
</style>