<script>
    let selected = "item2";
    const items = ["item1", "item2", "item3"];
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
    <div class={`selector ${selected}`} />
</div>

<style>
    .container {
        position: relative;
        display: flex;
        align-items: center;
        flex-direction: row;
        gap: 2rem;
        font-size: 24px;
        padding: 1%;
        width: 25rem;
        height: 2rem;
    }
    .menuItem {
        transition: 0.5s;
        user-select: none;
        display: flex;
        justify-content: center;
        width: 10rem;
        height: 3rem;
        border-radius: 10px;
        cursor: pointer;
        align-items: center;
    }

    .menuItem:hover {
        background: rgba(190, 190, 190, 0.1);
    }

    .item1 {
        --spacing: 1;
    }
    .item2 {
        --spacing: 2;
    }
    .item3 {
        --spacing: 3;
    }

    .selector {
        transition: 0.2s ease-out;
        position: absolute;
        width: 7rem;
        height: 3rem;
        border-radius: 10px;
        background: rgba(190, 190, 190, 0.2);
        top: 0.5rem;
        left: calc(var(--spacing, 1) * 33% - 29%);
        pointer-events: none;
    }
</style>
