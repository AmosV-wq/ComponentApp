<script>
    export let content = "Content";
</script>

<div class="container">
    <div class="button">
        {content}
    </div>
    <div class="block" />
    <div class="mag" />
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
        position: absolute;
        color: var(--primary);
        background: none;
        user-select: none;
        width: 8rem;
        height: 3rem;
        display: flex;
        align-items: center;
        justify-content: center;
        z-index: 4;
        transition: 0.2s;
    }

    .mag {
        position: absolute;
        border-radius: 50%;

        background: #ffffff15;
        width: 2rem;
        height: 2rem;
        z-index: 3;
        transform: translate(3.5rem, 1rem);
        backdrop-filter: blur(5px);
        pointer-events: none;

        transition: 0.2s;
    }

    .block {
        border-radius: 5px;
        position: absolute;
        background: var(--secondary);
        width: 8rem;
        height: 3rem;
        z-index: 1;
        transition: 0.2s;
    }

    .button:hover ~ .block {
        transform: translateY(0.5rem) scale(1.1);
    }

    .button:hover ~ .mag {
        transform: translate(0, -0.2rem);
        width: 7rem;
        height: 3rem;
        border-radius: 10px;
    }

    .button:hover {
        transform: scale(1.1);
    }

    .button:active ~ .mag {
        transform: translate(0, 0);
    }
</style>
