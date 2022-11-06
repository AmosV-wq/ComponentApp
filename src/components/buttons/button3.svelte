<script>
    export let content = "Content";
</script>

<div class="container">
    <div class="button">
        {content}
        <div class="shadow" />
    </div>
</div>

<style>
    .container {
        --primary: #000;
        --alt-primary: #242424;
        --secondary: #fff;

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
        color: var(--primary);
        border: 2px var(--primary) solid;
        user-select: none;
        width: 8rem;
        height: 3rem;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 0;
    }
    .shadow {
        width: inherit;
        height: inherit;
        background: yellow;
        opacity: 0.6;
        position: absolute;
        transform: translate(10px, 10px);
        pointer-events: none;
        transition: 0.2s;
        mix-blend-mode: darken;
    }

    .button:hover > .shadow {
        transform: translate(0);
        opacity: 0.8;
    }

    .button:active > .shadow {
        transform: translate(0);
        background: darkorange;
    }
</style>
