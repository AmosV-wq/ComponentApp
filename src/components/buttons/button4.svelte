<script>
    export let content = "Content";
</script>

<div class="container">
    <div class="button">
        {content}
    </div>
</div>

<style>
    .container {
        --primary: #000;
        --alt-primary: lightgrey;
        --secondary: #fff;

        display: flex;
        align-items: center;
        justify-content: center;
        width: 10%;
        height: 4rem;
        padding: 10px;
        background: var(--primary);
        border-radius: 5px;
    }

    .button {
        user-select: none;
        width: 8rem;
        height: 3rem;
        display: flex;
        align-items: center;
        justify-content: center;
        transition: 0.2s;
        background: var(--primary);
        border: var(--secondary) solid 1px;
    }

    .button:hover {
        box-shadow: 2px 2px 20px 1px purple, 2px -2px 20px 1px red,
            -2px -2px 20px 1px green, -2px 2px 20px 1px blue,
            -1px -1px 20px 1px yellow;
        mix-blend-mode: normal;
    }
</style>
