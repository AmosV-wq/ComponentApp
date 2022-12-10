<script>
    import PageTitle from "../components/pageTitle.svelte";
</script>

<PageTitle title="Paralax" />
<div class="container">
    {#each Array(10) as _}
        <div class="card">
            <img class="background" src="src/assets/background.jpg" alt="" />
            <div class="overlay">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Debitis, quisquam.
            </div>
        </div>
    {/each}
</div>

<style>
    .container {
        display: flex;
        justify-content: center;
        flex-direction: row;
        height: 100vh;
        overflow-y: auto;
        overflow-x: hidden;
        flex-wrap: wrap;
        gap: 10rem;
        perspective: 10px;
    }

    .card {
        position: relative;
        height: 25rem;
        aspect-ratio: 5/7;
        border: solid 5px white;
        perspective: 10px;
        overflow: hidden;
        transform-style: preserve-3d;
    }

    .overlay {
        box-sizing: border-box;
        padding: 1rem;
        position: absolute;
        display: flex;
        align-items: flex-end;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
        background: linear-gradient(
            0deg,
            rgba(0, 0, 0, 1) 0%,
            rgba(0, 0, 0, 0.5) 40%,
            rgba(0, 0, 0, 0) 100%
        );
        transition: 0.2s;
    }
    .card:hover > .overlay {
        font-size: large;
        height: 120%;
        top: -20%;
    }

    .background {
        width: 100%;
        height: 100%;
        object-fit: cover;
        border-radius: 10px;
        transform: translateZ(-5px) scale(4);
    }
</style>
