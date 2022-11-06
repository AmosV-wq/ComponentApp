<script>
    export let content = "Content";
</script>

<div class="container">
    <div class="button">
        {content}
        <div class="line horizontal" />
        <div class="line vertical" />
        <div class="overlay" />
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
        position: absolute;
        background: var(--primary);
        color: var(--secondary);
        user-select: none;
        width: 7rem;
        height: 3rem;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 0;
        transition: 0.2s;
    }

    .line {
        pointer-events: none;
        position: absolute;
        border: solid black;
        border-radius: 0;
        transition: 0.5s;
    }

    .horizontal {
        width: 6rem;
        height: 1rem;
        border-width: 2px 0px 2px 0px;
    }
    .vertical {
        width: 5rem;
        height: 2rem;
        border-width: 0px 2px 0px 2px;
    }

    .overlay {
        position: absolute;
        width: 7rem;
        height: 3rem;
        border: none;
        transform: scale(1.2);
        border: 2px black solid;
        opacity: 0;
        transition: 0.5s;
    }

    .button:hover > .line {
        width: 6rem;
        height: 2rem;
    }

    .button:hover > .overlay {
        opacity: 1;
        transform: scale(1);
    }

    .button:active > .overlay {
        transform: scale(0.9);
    }
    .button:active > .line {
        transform: scale(0.9);
    }
</style>
