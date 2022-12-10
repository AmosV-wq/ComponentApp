<script>
    import PageTitle from "../components/pageTitle.svelte";
</script>

<PageTitle title="Split" />
<div class="page">
    <div class="container">
        <div class="hoverable">
            <div class="text top">TEXT</div>
            <div class="text bottom">TEXT</div>
        </div>
        <div class="line" />
    </div>
</div>

<style>
    .page {
        width: 100vw;
        height: 90vh;
    }
    .container {
        height: 100%;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        line-height: 1;
    }

    .text {
        position: relative;
        font-size: 4em;
        text-align: center;
        transition: 0.2s;
        user-select: none;
    }

    .line {
        position: absolute;
        width: 0px;
        height: 2px;
        background: red;
        transition: 0.2s;
        border-radius: 9999;
    }

    .top {
        position: absolute;
        visibility: hidden;
        z-index: 3;
        height: 0.5em;
        overflow: hidden;
    }
    .hoverable {
        width: fit-content;
        height: fit-content;
    }

    .hoverable:hover > .top {
        visibility: visible;
        background: #242424;
        transform: skew(35deg);
        padding-left: 10px;
        padding-right: 10px;
    }

    .hoverable:hover > .bottom {
        z-index: 1;
        display: flex;
        align-items: flex-end;
        bottom: 0;
        overflow: hidden;
        transform: skew(30deg);
        padding-left: 10px;
        padding-right: 10px;
    }

    .hoverable:hover ~ .line {
        width: 200px;
        height: 4px;
        z-index: 99;
        pointer-events: none;
    }
</style>
