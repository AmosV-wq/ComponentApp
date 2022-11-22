<script>
    import Loader1 from "../components/loaders/loader1.svelte";
    import Loader2 from "../components/loaders/loader2.svelte";
    import Loader3 from "../components/loaders/loader3.svelte";
    import Loader4 from "../components/loaders/loader4.svelte";
    import PageTitle from "../components/pageTitle.svelte";
</script>

<PageTitle title="Loaders" />
<div class="page">
    <div class="container">
        <Loader1 />
    </div>
    <div class="container">
        <Loader2 />
    </div>
    <div class="container">
        <Loader3 />
    </div>
    <div class="container">
        <Loader4 />
    </div>
</div>

<style>
    * {
        padding: 0;
        box-sizing: border-box;
    }
    .page {
        width: 100vw;
        max-height: 100vh;
        overflow-y: scroll;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        padding: 1%;
    }

    .container {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 40vw;
        height: 30vh;
        background-color: #fff;
        border: 1px solid black;
        flex-grow: 1;
    }
</style>
