<script>
    import { Link } from "svelte-navigator";
</script>

<div class="titleBanner">
    <h1>Home</h1>
    <div class="cardContainer">
        <Link to="topBars">
            <div class="card">Top Bars</div>
        </Link>
        <Link to="buttons">
            <div class="card">Buttons</div>
        </Link>
        <Link to="cards">
            <div class="card">Cards</div>
        </Link>
    </div>
</div>

<style>
    :root {
        overflow: hidden;
    }

    .titleBanner {
        width: 100vw;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }

    h1 {
        font-size: 6rem;
    }

    .cardContainer {
        display: flex;
        flex-direction: row;
        gap: 2rem;
    }

    .card {
        width: 15vw;
        aspect-ratio: 4/3;
        display: flex;
        align-items: center;
        justify-content: center;
        border: 1px solid white;
        border-radius: 10px;
        transition: 0.2s;
        cursor: pointer;
        background: black;
    }

    .card:hover {
        box-shadow: 2px 2px 20px 1px purple, 2px -2px 20px 1px red,
            -2px -2px 20px 1px green, -2px 2px 20px 1px blue,
            -1px -1px 20px 1px yellow;
        mix-blend-mode: normal;

        font-size: 1.1rem;
        transform: scale(1.1);
    }
</style>
