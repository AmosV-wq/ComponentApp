<div class="container">
    <h1 class="title">Aradex</h1>
    <div class="trail" />
    <div class="path" />
    <div class="circle" />
</div>

<style>
    .title {
        color: #0e4961;
        font-size: 4rem;
    }
    .container {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .trail {
        position: absolute;
        border: #0e4961 dashed 1px;
        width: 190px;
        height: 180px;
        border-radius: 50%;
        transform: skew(50deg);
    }

    .circle {
        position: absolute;
        width: 15px;
        height: 25px;
        border-radius: 50%;
        background: #0e4961;
        animation: move 3s infinite linear;
    }

    @keyframes move {
        0% {
            transform: skew(50deg) rotate(0deg) translate(90px, 0px) scale(1);
        }
        25% {
            transform: skew(50deg) rotate(90deg) translate(90px, 0px) scale(1.5);
        }
        50% {
            transform: skew(50deg) rotate(180deg) translate(90px, 0px)
                scale(0.75);
        }
        75% {
            transform: skew(50deg) rotate(270deg) translate(90px, 0px)
                scale(0.6);
        }
        100% {
            transform: skew(50deg) rotate(360deg) translate(90px, 0px)
                scale(0.75);
        }
    }
</style>
