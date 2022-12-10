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
        font-size: 44px;
        padding: 1%;
        width: 40vw;
        height: 2rem;
    }
    .menuItem {
        flex-grow: 1;
        transition: 0.5s;
        user-select: none;
        display: flex;
        justify-content: center;
        cursor: pointer;
    }

    .shrink {
        font-size: 24px;
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
        width: 10px;
        height: 10px;
        background: red;
        border-radius: 50%;
        top: 4rem;
        left: calc(var(--spacing, 1) * 30% - 10%);
    }
</style>
