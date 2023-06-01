<script>
import CardComponents from "./CardComponents.vue";
export default {
    name: 'AppMain',
    data(){
        return{
            comics: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://img.gocollect.com/eyJidWNrZXQiOiJnb2NvbGxlY3QuaW1hZ2VzLnB1YiIsImtleSI6IjAwMjE4MGM3LTJhYTctNDZjNC05MjUyLTZmYTQ4NDJkMzAyYS5qcGciLCJlZGl0cyI6W119",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.comicsbox.it/cover_dc/BTMSUP_001.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://i0.wp.com/batman-news.com/wp-content/uploads/2020/09/Batman-Superman-Annual-1.jpg?fit=696%2C1070&quality=80&strip=info&ssl=1",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.badtaste.it/fumetti/wp-content/uploads/sites/3/2020/06/batman-thejoker-warzone-001-ben-oliver.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://pbs.twimg.com/media/EdKd9M_VAAA5Lm4?format=jpg&name=4096x4096",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://m.media-amazon.com/images/I/51sZeblq1fL.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://img.gocollect.com/eyJidWNrZXQiOiJnb2NvbGxlY3QuaW1hZ2VzLnB1YiIsImtleSI6IjUxOTExM2U0LTA0ZDEtNDBlMy05NjBkLWE0NWZlOWJiODFhMC5qcGciLCJlZGl0cyI6W119",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        }
    },
    components:{
    CardComponents
}
}
</script>
<template>
    <main>
        <section class="jumbotron">
            <button>current series</button>
        </section>
        <div class="container">
            <section>
                <CardComponents
                v-for="element in comics"
                :imgSrc="element.thumb"
                :imgTitle="element.series" />
            </section>
            <div>
                <button>Load more</button>
            </div>
        </div>
    </main>
</template>
<style lang="scss" scoped>
    main{
        min-height: 850px;
        background-color: #1c1c1c;
        // padding: 30px 0;
        section.jumbotron{
            height: 40vh;
            background-image: url('../assets/img/jumbotron.jpg');
            background-size: cover;
            background-repeat: no-repeat;
            margin-bottom: 30px;
        }
        div.container{
            max-width: 1200px;
            margin: 0 auto;
            section{
                display: flex;
                flex-wrap: wrap;
                div.card{
                    width: calc(100% / 6);
                    img{
                        height: 50%;
                    }
                    h4{
                        text-transform: uppercase;
                        color: white;
                    }
                }
            }
        }
    }
</style>