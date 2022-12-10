<script>
    import PageTitle from "../components/pageTitle.svelte";
    import TopBar1 from "../components/topbars/topBar1.svelte";
    import TopBar2 from "../components/topbars/topBar2.svelte";
    import TopBar3 from "../components/topbars/topBar3.svelte";
</script>

<div class="container">
    <PageTitle title="TopBars" />
    <TopBar1 />
    <TopBar2 />
    <TopBar3 />
</div>

<style>
    .container {
        width: 100vw;
        height: 100vh;
        gap: 5rem;
        display: flex;
        flex-direction: column;
    }
</style>
