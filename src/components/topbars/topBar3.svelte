<script>
    let selected = "item2";
    const items = ["item1", "item2", "item3"];
    const navigate = (direction) => {
        let index = (items.indexOf(selected) + direction) % items.length;
        if (index === -1) {
            index = items.length - 1;
        }

        return items[index];
    };
</script>

<div class="outer">
    <div class="button" on:click={() => (selected = navigate(-1))}>Left</div>
    <div class="container">
        <div class={`selection ${selected}`}>
            {#each items as item}
                <div
                    class={`menuItem ${
                        selected == item ? "selected" : "shrink"
                    }`}
                    on:click={() => (selected = item)}
                    on:keydown={() => (selected = item)}
                >
                    {item}
                </div>
            {/each}
        </div>
    </div>
    <div class="button" on:click={() => (selected = navigate(1))}>Right</div>
</div>

<style>
    .outer {
        display: flex;
        flex-direction: row;
        margin-left: 10%;
        gap: 10px;
        align-items: center;
    }

    .button {
        border-radius: 50%;
        width: 3rem;
        height: 3rem;
        background: grey;
        color: black;
        display: flex;
        align-items: center;
        justify-content: center;
        transition: 0.2s;
        user-select: none;
    }

    .item1 {
        --spacing: 1;
    }
    .item2 {
        --spacing: 0;
    }
    .item3 {
        --spacing: -1;
    }

    .container {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: row;
        gap: 2rem;
        font-size: 24px;
        padding: 1%;
        width: 5rem;
        height: 2rem;
        background: grey;
        border-radius: 10px;
        color: black;
        overflow: hidden;
    }

    .menuItem {
        user-select: none;
    }

    .selection {
        position: relative;
        display: flex;
        flex-direction: row;
        gap: 2rem;
        align-items: center;
        justify-content: center;
        left: calc(var(--spacing, 1) * 6rem);
        transition: 0.2s ease-in-out;
    }
</style>
