<script>
    import PageTitle from "../components/pageTitle.svelte";
    import Icon from "@iconify/svelte";

    let active = 0;
    let elementList = ["one", "two", "three"];
    let element;
    let nextElement;
    let disabled = "";
    const showNext = () => {
        element = document.getElementById(elementList[active]);
        element.classList.replace("active", "right");
        if (active + 1 >= elementList.length) {
            active = 0;
        } else {
            active += 1;
        }
        nextElement = document.getElementById(elementList[active]);
        nextElement.classList.add("left");
        disabled = "disabled";

        setTimeout(() => {
            element.classList.remove("right");
            nextElement.classList.replace("left", "active");
            disabled = "";
        }, 500);
    };

    const showPrev = () => {
        element = document.getElementById(elementList[active]);
        element.classList.replace("active", "left");
        if (active - 1 < 0) {
            active = elementList.length - 1;
        } else {
            active -= 1;
        }

        nextElement = document.getElementById(elementList[active]);
        nextElement.classList.add("right");
        disabled = "disabled";

        setTimeout(() => {
            element.classList.remove("left");
            nextElement.classList.replace("right", "active");
            disabled = "";
        }, 500);
    };
</script>

<div class="page">
    <PageTitle title="Cards" />
    <div class="container active" id="one">
        <div class="card big" />
        <div class="card big" />
        <div class="card big" />
        <div class="card small" />
        <div class="card small" />
        <div class="card small" />
        <div class="card small" />
        <h1 class="title">One</h1>
    </div>
    <div class="container" id="two">
        <div class="card big" />
        <div class="card big" />
        <div class="card big" />
        <div class="card small" />
        <div class="card small" />
        <div class="card small" />
        <div class="card small" />
        <h1 class="title">Two</h1>
    </div>
    <div class="container" id="three">
        <div class="card big" />
        <div class="card big" />
        <div class="card big" />
        <div class="card small" />
        <div class="card small" />
        <div class="card small" />
        <div class="card small" />
        <h1 class="title">Three</h1>
    </div>
    <div class="controls">
        <div
            class={"button " + disabled}
            on:keydown={() => showPrev()}
            on:click={() => showPrev()}
        >
            <Icon icon="eva:arrow-back-outline" />
        </div>
        <div
            class={"button " + disabled}
            on:keydown={() => showNext()}
            on:click={() => showNext()}
        >
            <Icon icon="eva:arrow-forward-outline" />
        </div>
    </div>
</div>

<style>
    .title {
        position: absolute;
        transition: 0.2s;
        top: -30%;
        pointer-events: none;
    }

    .disabled {
        opacity: 0.5;
        pointer-events: none;
    }

    .page {
        display: flex;
        flex-direction: column;
        justify-content: center;
        gap: 25vh;
    }

    .container {
        position: absolute;
        display: flex;
        align-items: center;
        justify-content: center;
        transition: 0.2s;

        transform: scale(0);
        opacity: 0;
        aspect-ratio: 5/7;
        height: 20rem;
        top: 30%;
        left: 50vw;
        align-self: center;
    }

    .active {
        opacity: 1;
        left: 40%;
        transform: scale(1);
    }

    .left {
        left: 20%;
    }

    .right {
        left: 60%;
    }

    .controls {
        position: absolute;
        top: 80%;
        display: flex;
        flex-direction: row;
        gap: 2rem;
        left: 44%;
    }

    .button {
        border-radius: 50%;
        width: 3rem;
        height: 3rem;
        background: grey;
        color: white;
        font-size: 32px;
        display: flex;
        align-items: center;
        justify-content: center;
        transition: 0.2s;
    }

    .button:hover {
        background: darkgrey;
    }

    .card {
        position: absolute;
        height: 20rem;
        aspect-ratio: 5/7;
        background: white;
        border-radius: 10px;
        transition: 0.5s;
    }

    .small {
        height: 8rem;
    }

    .big:nth-child(1) {
        transform: rotate(5deg);
        background: grey;
        z-index: 2;
    }

    .big:nth-child(2) {
        transform: rotate(-8deg);
        background: black;
        z-index: 4;
    }

    .big:nth-child(3) {
        background: antiquewhite;
        z-index: 6;
    }

    .small:nth-child(4) {
        z-index: 1;
    }

    .small:nth-child(5) {
        z-index: 3;
    }

    .small:nth-child(6) {
        z-index: 5;
    }

    .small:nth-child(7) {
        z-index: 5;
    }

    .container:hover > .big:nth-child(1) {
        transform: translate(-4rem, 2rem) rotate(-20deg);
    }

    .container:hover > .big:nth-child(2) {
        transform: translate(0rem, 2rem) rotate(0deg);
    }

    .container:hover > .big:nth-child(3) {
        transform: translate(4rem, 2rem) rotate(20deg);
    }

    .container:hover > .small:nth-child(4) {
        transform: translate(-20rem, 1rem) rotate(-40deg);
    }

    .container:hover > .small:nth-child(5) {
        transform: translate(12rem, -14rem) rotate(-10deg);
    }

    .container:hover > .small:nth-child(6) {
        transform: translate(20rem, 7rem) rotate(40deg);
    }

    .container:hover > .small:nth-child(7) {
        transform: translate(-10rem, -14rem) rotate(-10deg);
    }
</style>
