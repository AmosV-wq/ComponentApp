<script>
    import { Link } from "svelte-navigator";
    import Button1 from "../components/buttons/button1.svelte";
    import Button2 from "../components/buttons/button2.svelte";
    import Button3 from "../components/buttons/button3.svelte";
    import Button4 from "../components/buttons/button4.svelte";
    import Button5 from "../components/buttons/button5.svelte";
    import Button6 from "../components/buttons/button6.svelte";
    import Button7 from "../components/buttons/button7.svelte";
    import Button8 from "../components/buttons/button8.svelte";
    import PageTitle from "../components/pageTitle.svelte";
</script>

<div class="container">
    <PageTitle title="Buttons" />
    <div class="content">
        <Button1 />
        <Button2 />
        <Button3 />
        <Button4 />
        <Button5 />
        <Button6 />
        <Button7 />
        <Button8 />
    </div>
</div>

<style>
    .container {
        width: 100vw;
        height: 100vh;
        display: flex;
        flex-direction: column;
        gap: 2rem;
    }

    .content {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        align-items: center;
        gap: 2rem;
    }
</style>
