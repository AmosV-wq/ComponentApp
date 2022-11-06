<script>
    import Icon from "@iconify/svelte";
    import { Link } from "svelte-navigator";

    export let title;
</script>

<div class="container">
    <div class="top">
        <Link to="/">
            <div class="icon">
                <Icon icon="eva:arrow-back-outline" />
            </div>
        </Link>
        <h1>{title}</h1>
    </div>
</div>

<style>
    .top {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 10px;
    }
    .icon {
        font-size: 32px;
        transition: 0.2s;
    }

    .icon:hover {
        font-size: 40px;
    }
</style>
