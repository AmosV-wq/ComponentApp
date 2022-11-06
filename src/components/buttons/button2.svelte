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
        --alt-primary: #333;
        --secondary: #01b0d3;
        --text: #fff;

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
        user-select: none;
        border-radius: 5px;
        background: var(--secondary);
        color: var(--primary);
        padding: 5%;
        width: 8rem;
        height: 3rem;
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 10px;
        font-size: 16px;
        color: var(--text);
        box-shadow: 5px 5px var(--alt-primary);
        transition: 0.2s;
    }

    .button:active {
        box-shadow: 2px 2px var(--alt-primary);
        transform: translate(3px, 3px);
    }
</style>
