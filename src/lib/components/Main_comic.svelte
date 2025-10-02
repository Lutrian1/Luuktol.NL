<header>
    <div class="top-box--1-for-ani">
        <img src="/assests/pics/luuk-1.svg" alt="A hand-drawn picture of Luuk greating you" width="200" height="200">
    </div>
    <div class="top-box--2-for-ani">
        <img src="/assests/pics/luuk-2.svg" alt="A hand-drawn picture of Luuk point down and showing you you should look at his work" width="200" height="200">
    </div>
</header>

<nav>

    <article class="nav-box-1">
        <div class="border-on-text">
            <a href="/learning-journal">
                <h1>Learning Journal</h1>
            </a>
        </div>
        <aside class="info-1" hidden>
            <p></p>
        </aside>
    </article>

    <article class="nav-box-2">
        <div class="border-on-text">
            <a href="/mijn-werk">
                <h2>My work</h2>
            </a>
        </div>
        <aside class="info-2" hidden>
            <p></p>
        </aside>
    </article>

    <article class="nav-box-3">
        <div class="border-on-text">
            <a href="/blog">
                <h3>Blog</h3>
            </a>
        </div>
        <aside class="info-2" hidden>
            <p></p>
        </aside>
    </article>

    <article class="nav-box-4">
        <div class="border-on-text">
            <a href="/blog">
                <h3>Extra's</h3>
            </a>
        </div>
        <aside class="info-2" hidden>
            <p></p>
        </aside>
    </article>
</nav>

<style>

main{
    background-color: black;
}

header{
    display: grid;
    grid-template-areas: 
    "box-1"
    "box-2";
        @media (min-width: 970px) {
            grid-template-areas: 
            "box-1 box-2"
        }
}

nav{  
    display: grid; 
    grid-template-areas: 
    "box-3"
    "box-4"
    "box-5"
    "box-6"; 
        @media (min-width: 600px) {
            grid-template-areas: 
            "box-3 box-4"
            "box-5 box-6"; 
        }
    margin-left: calc(var(--border-entire-page) - 6px);
}

.top-box--1-for-ani{
    grid-area: box-1; 
    height: 45vh;
    display: flex;
    justify-content: center;
    align-items: flex-end;
    margin: 0;
    width: 100%;
    background-image: url("/assests/pics/bg-yellow-variant.svg");
    background-size: cover;
    background-repeat: no-repeat;
    img{
        z-index: 8;
        margin-bottom: calc(-10px);
        @media (min-width: 350px) {
            height: 270px;
            width: 270px;
        }
        @media (min-width: 970px) {
            height: 350px;
            width: 350px;
        }
    }
}

.top-box--2-for-ani{
    grid-area: box-2; 
    height: 45vh;
    display: flex;
    justify-content: center;
    align-items: flex-end;
    width: 100%;
    background-image: url("/assests/pics/bg-blue-variant.svg");
    background-size: cover;
    background-repeat: no-repeat;
    img{
        z-index: 8;
        margin-bottom: calc(-65px - 10px);
        @media (min-width: 350px) {
            height: 350px;
            width: 350px;
        }
        @media (min-width: 970px) {
            height: 450px;
            width: 450px;
            margin-bottom: calc(-75px - 10px);
        }
    }
}
.nav-box-1, .nav-box-2, .nav-box-3, .nav-box-4{
    width: 100%;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;

    a{
        font-size: clamp(2rem, 6vw, 3rem);
        text-decoration: none;
        color: black;
        z-index: 9;
    }

        @supports (-webkit-text-stroke-color: black) or (-webkit-background-clip: text) {
            a{  
                color: transparent;
                -webkit-text-stroke-color: black;
                -webkit-text-stroke-width: 1px;
            }
    }
}

.nav-box-1{
    grid-area: box-3; 
    height: 50vh;
    background-image: url("/assests/pics/bg-green-variant.svg");
    background-size: cover;
    background-repeat: no-repeat;
}

.nav-box-2{
    grid-area: box-4; 
    height: 50vh;
    background-image: url("/assests/pics/bg-pink-variant.svg");
    background-size: cover;
    background-repeat: no-repeat;
}

.nav-box-3{
    grid-area: box-5; 
    height: 50vh;
    background-image: url("/assests/pics/bg-red-variant.svg");
    background-size: cover;
    background-repeat: no-repeat;
}

.nav-box-4{
    grid-area: box-6; 
    height: 50vh;
    background-image: url("/assests/pics/bg-purple-variant.svg");
    background-size: cover;
    background-repeat: no-repeat;
}


/*----------------------------------- Border page --------------------------------------*/

.border-entire-page {
    border: var(--border-entire-page) solid;
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    box-sizing: border-box; 
    background-image: url('/assests/noise.svg');
    z-index: 7;
    pointer-events: none;
}

/*----------------------------------- COPYRIGHT AND DISCLAIMER--------------------------------------*/

.copyright{
    border: solid 8px;
    display: flex;
    justify-content: center;
    width: 160px;
    height: 27px;
    position: fixed;
    margin: 0;
    background-color: var(--primary-color);
    z-index: 9;
    bottom: 0;
    right: 0;
}


.disclaimer{
    border: solid 8px;
    display: flex;
    justify-content: center;
    width: 50px;
    height: fit-content;
    position: fixed;
    margin: 0;
    background-color: var(--primary-color);
    z-index: 9;
    bottom: 0;
    left: 0;
    font-size: 9px;
}

/*----------------------------------- SUPPORTS QUERY: THIS DEFINES THE SITE SHAPE --------------------------------------*/

@supports (clip-path: shape(from 0% 0%,hline to 93.74%,line to 100% 100%,line to 0% 89.01%,vline to 0%,close)){
    .top-box--1-for-ani{
        clip-path: shape(from 0% 0%,hline to 93.74%,line to 100% 100%,line to 0% 89.01%,vline to 0%,close);
        background-color: #FFF185;
        img{
            margin-bottom: 0;
        }
    }
    .top-box--2-for-ani{
        clip-path: shape(from 0% 0%,hline to 100%,vline to 100%,line to 4.28% 87.66%,line to 0% 0%,close);
        background-color: #A4FFF4;
    }
    .nav-box-1, .nav-box-2, .nav-box-3, .nav-box-4, .top-box--1-for-ani, .top-box--2-for-ani{
        overflow: hidden;
        background-image: none;
    }
    .nav-box-1{
        clip-path: shape(from 0% 0%,line to 100% 12.08%,line to 92.9% 90.63%,line to 0% 100%,vline to 0%,close);
        background-color: #A7FFBE;
    }
    .nav-box-2{
        clip-path: shape(from 12.03% 0%,line to 98.66% 6.57%,line to 100% 92.05%,line to 0% 100%,line to 12.03% 0%,close);
        background: #D466AF;
    }
    .nav-box-3{
        clip-path: shape(from 0% 8.68%,line to 89.56% 0%,line to 100% 100%,hline to 0%,vline to 8.68%,close);
        background: #FF8F8F;
    }
    .nav-box-4{
        clip-path: shape(from 0% 14.98%,line to 100% 0%,vline to 100%,hline to 5.51%,line to 0% 14.98%,close);
        background: #a2d8f1;
    }
}

</style>