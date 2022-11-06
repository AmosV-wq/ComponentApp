<script>
    export let content = "Content";
</script>

<div class="container light" id="container">
    <div class="button">
        {content}
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
        background: var(--primary);
        border-radius: 10px;
    }

    .button {
        border-radius: 5px;
        background: var(--primary);
        color: var(--secondary);
        padding: 2%;
        width: 8rem;
        height: 3rem;
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 10px;

        user-select: none;

        box-shadow: 0 0 10px 1px var(--secondary);
        border-bottom: 4px solid var(--alt-primary);
        border-left: 2px solid var(--alt-primary);
        border-right: 2px solid var(--alt-primary);

        transition: 0.1s;

        font-family: "JetBrains Mono", monospace;
    }

    .button:hover {
        transform: translateY(-2px);
        box-shadow: 0 1px 10px 1px var(--secondary);
    }

    .button:active {
        margin: 12px;
        border: none;
        transform: translateY(4px);
        box-shadow: var(--alt-primary) 0 3px 7px inset;
    }
</style>
