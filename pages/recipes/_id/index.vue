<template>
    
    
    <section class="single-recipe">
        <p> {{ $route.params.id }} </p>
        <h1> {{ recipe.title }} </h1>
        <div>
            <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title">
        </div>
        <p> {{ recipe.descriptionText }} </p>
    </section>
</template>

<script>
export default {
 asyncData(context) {
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                resolve({
                    recipe: [
                        {
                            id: '1',
                            title: 'Delicious pizza',
                            previewText: 'Nice pizza',
                            thumbnail: 'https://berlinfoodstories.com/wp-content/uploads/2015/04/Zur-Haxe-Berlin-Schinkenhaxe.jpg',
                            descriptionText: 'This is a delicious meal'
                        },
                        {
                             id: '2',
                            title: 'Kebap',
                            previewText: 'Turkish finest',
                            thumbnail: 'https://www.ayewanderful.com/wp-content/uploads/2017/05/Tacos-with-Mushroom-Pibil.jpg',
                            descriptionText: 'This is a delicious meal'
                        }
                    ].find(el => el.id === context.params.id)
                })
            }, 1500);
        })
    }
}
</script>

<style>
.single-recipe {
    display: flex;
    justify-content: center;
    flex-flow: column;
    align-items: center;
    text-align: center;

}

.recipe-image {
    width: 100%;
}
</style>
