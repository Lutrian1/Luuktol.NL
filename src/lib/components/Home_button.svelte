<script>
    import { home_button_SVG } from '$lib';
</script>

<a href="/" class="home-button">
    <img src="{home_button_SVG}" alt="" class="home-text">
</a>

<style>

.home-button{
    border: solid 10px;
    background-color: var(--button-background-color);
    position: fixed;
    display: flex;
    top: 0;
    left: 0;
    text-decoration: none;
    color: black;
    z-index: 10;

    .home-text{
        position: relative;
        top: 10px;
        padding: 3px;
        height: 70px;

            @media (min-width: 600px) {
                height: 108px;
            }
    }
}

.home-button:hover{
    background-color: #a08fff;
}

</style>