<script>
    export let content = "Content";
</script>

<div class="container">
    <div class="glow">
        <div class="button">
            {content}
        </div>
    </div>
</div>

<style>
    .container {
        --primary: #fff;
        --alt-primary: lightgrey;
        --secondary: #000;

        display: flex;
        align-items: center;
        justify-content: center;
        width: 10%;
        height: 4rem;
        padding: 10px;
        background: var(--secondary);
        border-radius: 10px;
    }

    .button {
        background: var(--secondary);
        user-select: none;
        width: 8rem;
        height: 3rem;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 0;
        transition: 0.2s;
    }

    .button:hover {
        background: none;
    }
    .glow {
        padding: 2px;
        background-image: linear-gradient(
            144deg,
            #af40ff,
            #5b42f3 50%,
            #00ddeb
        );
    }
</style>
