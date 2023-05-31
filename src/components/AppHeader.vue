<script>
export default {
    name: 'AppHeader',
    // data header link

    data(){
        return{
            headerLinks: [
                {
                    linkName: 'characters',
                    hrefLink: '#'
                }, {
                    linkName: 'comics',
                    hrefLink: '#'
                }, {
                    linkName: 'movies',
                    hrefLink: '#'
                }, {
                    linkName: 'tv',
                    hrefLink: '#'
                }, {
                    linkName: 'games',
                    hrefLink: '#'
                }, {
                    linkName: 'collectibles',
                    hrefLink: '#'
                }, {
                    linkName: 'videos',
                    hrefLink: '#'
                }, {
                    linkName: 'fans',
                    hrefLink: '#'
                }, {
                    linkName: 'news',
                    hrefLink: '#'
                }, {
                    linkName: 'shop',
                    hrefLink: '#'
                }
                
            ]
        }
    }
}

</script>
<!----------------------------------------------------------------- -->

<template>
<header>
        <div class="container">
            <img src="../assets/img/dc-logo.png" alt="logo">
            <nav>
                <ul>
                   <li  v-for="element in headerLinks">
                        <a :href="element.hrefLink">
                            {{ element.linkName }}
                        </a>
                    <!-- <li>
                        <a href="#">characters</a>
                    </li>
                    <li>
                        <a href="#">comics</a>
                    </li>
                    <li>
                        <a href="#">movies</a>
                    </li>
                    <li>
                        <a href="#">tv</a>
                    </li>
                    <li>
                        <a href="#">games</a>
                    </li>
                    <li>
                        <a href="#">collectibles</a>
                    </li>
                    <li>
                        <a href="#">videos</a>
                    </li>
                    <li>
                        <a href="#">fans</a>
                    </li>
                    <li>
                        <a href="#">news</a>
                    </li>
                    <li>
                        <a href="#">shop</a> -->
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header{
        height: 70px;
        padding: 10px;
        margin-bottom: 6px;
        div{
            max-width: 1000px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 100%;
            img{
                height: 100%;
            }
            nav{
                ul{
                    display: flex;
                    justify-content: center;
                    li{
                        list-style: none;
                        padding: 30px 15px;
                        color: black;
                        &:hover{
                            color: #0282f9;
                            border-bottom: 5px solid #11599c;
                        }
                        a{
                            text-decoration: none;
                            color: inherit;
                            text-transform: uppercase;
                        }
                    }
                }
            }
        }
    }
</style>