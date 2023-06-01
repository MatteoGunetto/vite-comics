<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            footerLinks: [
                {
                    linkName: 'digital comics',
                    urlImg: 'buy-comics-digital-comics.png',
                    hrefLink: '#'
                }, {
                    linkName: 'dc merchandise',
                    urlImg: 'buy-comics-merchandise.png',
                    hrefLink: '#'
                }, {
                    linkName: 'subscription',
                    urlImg: 'buy-comics-subscriptions.png',
                    hrefLink: '#'
                }, {
                    linkName: 'comic shop locator',
                    urlImg: 'buy-comics-shop-locator.png',
                    hrefLink: '#'
                }, {
                    linkName: 'dc power visa',
                    urlImg: 'buy-dc-power-visa.svg',
                    hrefLink: '#'
                }
            ]
        }
    },
    methods: {
        getImgPath(imgPath){
            return new URL(imgPath, import.meta.url).href;
        }
    }
}

</script>
<template>
   <footer>
        <div class="container">
            <section class="first-section">
                <nav>
                    <ul>
                        <li v-for="element in footerLinks">
                            
                            <img :src="getImgPath(`../assets/img/${element.urlImg}`)" :alt="element.linkName">
                            <a :href="element.hrefLink">
                            {{ element.linkName }}</a>
                        </li>    
                        
                    </ul>
                </nav>
            </section>
            <section class="second-section">
                <div class="second-container">
                    <div class="menu">
                        <div>
                        <ul>
                            <li>
                                <h3>dc comics</h3>
                            </li>
                            <li>
                                <a href="#">Characters</a>
                            </li>
                            <li>
                                <a href="#">Comics</a>
                            </li>
                            <li>
                                <a href="#">Movies</a>
                            </li>
                            <li>
                                <a href="#">TV</a>
                            </li>
                        <li>
                            <a href="#">Games</a>
                        </li>
                        <li>
                            <a href="#">Video</a>
                        </li>
                        <li>
                            <a href="#">News</a>
                        </li>
                    </ul>
                    <ul>
                        <li>
                            <h3>shop</h3>
                        </li>
                        <li>
                            <a href="#">Shop DC</a>
                        </li>
                        <li>
                            <a href="#">Shop DC Collectibles</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <ul>
                        <li>
                            <h3>dc</h3>
                        </li>
                        <li>
                            <a href="#">Terms Of Use</a>
                        </li>
                        <li>
                            <a href="#">Privacy policy (New)</a>
                        </li>
                        <li>
                            <a href="#">Ad Choices</a>
                        </li>
                        <li>
                            <a href="#">Advertising</a>
                        </li>
                        <li>
                            <a href="#">Jobs</a>
                        </li>
                        <li>
                            <a href="#">Subscription</a>
                        </li>
                        <li>
                            <a href="#">Talent Workshop</a>
                        </li>
                        <li>
                            <a href="#">CPSC Certificates</a>
                        </li>
                        <li>
                            <a href="#">Ratings</a>
                        </li>
                        <li>
                            <a href="#">Shop Help</a>
                        </li>
                        <li>
                            <a href="#">Contact Us</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <ul>
                        <li>
                            <h3>sites</h3>
                        </li>
                        <li>
                            <a href="#">DC</a>
                        </li>
                        <li>
                            <a href="#">MAD Magazine</a>
                        </li>
                        <li>
                            <a href="#">DC Kids</a>
                        </li>
                        <li>
                            <a href="#">DC Universe</a>
                        </li>
                        <li>
                            <a href="#">DC Power Visa</a>
                        </li>
                        
                    </ul>
                </div>
                    </div>
                    <div class="img-logo">
                        <img src="../assets/img/dc-logo-bg.png" alt="">
                    </div>
                </div>
            
                
                   
            </section>
            <section class="third-section">
                <div>
                    <div>
                        <button>
                            sign-up now!
                        </button>
                    </div>
                    <div>
                        <a href="#">follow us</a>
                        <img src="../assets/img/footer-facebook.png" alt="facebook">
                        <img src="../assets/img/footer-twitter.png" alt="twitter">
                        <img src="../assets/img/footer-youtube.png" alt="youtube">
                        <img src="../assets/img/footer-pinterest.png" alt="pinterest">
                        <img src="../assets/img/footer-periscope.png" alt="periscope">
                    </div>
                </div>
            </section>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
footer{
    height: 850px;
    
    div.container{
        height: 100%;
        section.first-section{
            height: 170px;
            background-color: #0282f9;
            display: flex;
            text-align: center;
            justify-content: center;
            z-index: 1;
            position: relative;
            nav{
                height: 100%;
                width: 1200px;
                margin: 0 auto;
                ul{
                    display: flex;
                    text-align: center;
                    justify-content: space-around;
                    height: 100%;
                    li{
                        list-style: none;
                        height: 100%;
                        display: flex;
                        align-items: center;
                        justify-content: space-between;
                        padding: 0 20px;
                        a{
                            text-decoration: none;
                            color: white;
                            text-transform: uppercase;
                            font-size: 16px;
                            padding-left: 10px;
                        }
                        img{
                            height: 40%;
                        }
                    }
                }
            }
        }

        // .container{
        //     height: 530px;
        //     max-width: 2000px;
        //     margin: 0 auto;
        //     display: flex;
        //     padding: 40px 0;
        //     overflow: hidden;
        //     gap: 300px;
        // }
        .menu{
            display: flex;
            gap: 20px;
            padding-left: 330px;
        }
        .second-container{
            height: 530px;
            max-width: 2000px;
            margin: 0 auto;
            display: flex;
            padding: 40px 0;
            overflow: hidden;
            gap: 100px;
        }
        section.second-section{
            background-image: url('../assets/img/footer-bg.jpg');
            background-repeat: no-repeat;
            background-size: cover;
            display: flex;

                div{
                    margin-right: 25px;
                    ul{
                        li{
                            color: white;
                            list-style: none;
                            h3{
                                text-transform: uppercase;
                                margin-bottom: 8px;
                            }
                            a{
                                color: inherit;
                                margin-bottom: 5px;
                                text-decoration: none;
                                font-size: 15px;
                            }
                        }
                    }
                    ul:first-of-type{
                        margin-bottom: 15px;
                    }
                }
                div:last-of-type{
                    flex-grow: 1;
                }

                img{
                    width: 650px;

                }
        }
        section.third-section{
            height: 150px;
            background-color: #303030;
            div{
                max-width: 1200px;
                height: 100%;
                margin: 0 auto;
                display: flex;
                justify-content: space-between;
                align-items: center;
                div:first-child{
                    flex-grow: 1;
                    button{
                        color: white;
                        text-transform: uppercase;
                        border: 2px solid #0282f9;
                        padding: 10px 15px;
                        background-color: transparent;
                        cursor: pointer;
                    }
                }
                div:last-child{
                    a{
                        text-decoration: none;
                        color: #0282f9;
                        text-transform: uppercase;
                        margin-right: 5px;
                    }
                    img{
                        height: 25px;
                        margin: 0 5px;
                    }
                }
            }
        }
    }
}
</style>







    