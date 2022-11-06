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
        user-select: none;
        width: 8rem;
        height: 3rem;
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>
