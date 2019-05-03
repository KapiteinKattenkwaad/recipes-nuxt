<template>
    <section class="recipes">

        <Recipe 
            v-for="recipe in recipes" :key="recipe.id"
            :thumbnail="recipe.thumbnail"
            :title="recipe.title"
            :previewText="recipe.previewText"
            :id="recipe.id"
             />
    
        
    </section>
</template>

<script>
import Recipe from '@/components/Recipe'
export default {
    components: {
        Recipe
    },
    asyncData() {
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                resolve({
                    recipes: [
                        {
                            id: '1',
                            title: 'Delicious pizza',
                            previewText: 'Nice pizza',
                            thumbnail: 'https://berlinfoodstories.com/wp-content/uploads/2015/04/Zur-Haxe-Berlin-Schinkenhaxe.jpg'
                        },
                        {
                             id: '2',
                            title: 'Kebap',
                            previewText: 'Turkish finest',
                            thumbnail: 'https://www.ayewanderful.com/wp-content/uploads/2017/05/Tacos-with-Mushroom-Pibil.jpg'
                        }
                    ]
                })
            }, 1500);
        })
    }
};
</script>

<style scoped>

.recipes {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
}





</style>
