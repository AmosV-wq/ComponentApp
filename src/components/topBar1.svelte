<script>
    let selected = "Item 2";
    const items = ["Item 1", "Item 2", "Item 3"];
</script>

<div class="container">
    {#each items as item}
        <div
            class={`menuItem ${selected == item ? "selected" : "shrink"}`}
            on:click={() => (selected = item)}
            on:keydown={() => (selected = item)}
        >
            {item}
        </div>
    {/each}
    <div class="selector" />
</div>

<style>
    .container {
        flex-grow: 1;
        display: flex;
        align-items: center;
        flex-direction: row;
        gap: 2rem;
        font-size: 44px;
        padding: 1%;
        width: 100vw;
        height: 2rem;
    }
    .menuItem {
        transition: 0.2s;
        user-select: none;
    }

    .shrink {
        font-size: 24px;
    }

    .selector {
        transition: 0.2s;
        transform: translate(30px, 40px);
        position: absolute;
        width: 10px;
        height: 10px;
        background: red;
        border-radius: 50%;
    }
</style>
