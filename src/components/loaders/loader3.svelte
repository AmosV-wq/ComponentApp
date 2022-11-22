<div class="container">
    <div class="circle" />
    <div class="outer">
        <div class="circle small" />
    </div>
    <div class="outer">
        <div class="circle small" />
    </div>
</div>

<style>
    .container {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .circle {
        position: absolute;
        background-color: #0e4961;
        border-radius: 50%;
        width: 55px;
        height: 55px;
    }
    .outer {
        position: absolute;
        width: 80px;
        height: 80px;
        animation: rotate 2s linear infinite;

        border: 1px black solid;
        border-radius: 50%;
    }
    .outer:nth-child(odd) {
        width: 110px;
        height: 110px;
        animation-direction: reverse;
        animation-duration: 3s;
    }

    .small {
        width: 15px;
        height: 15px;
    }

    .outer:nth-child(even) > .small {
        transform: translate(4px, 4px);
    }

    .outer:nth-child(odd) > .small {
        transform: translate(8px, 8px);
    }

    @keyframes rotate {
        0% {
            transform: rotate(0deg);
        }
        100% {
            transform: rotate(360deg);
        }
    }
</style>
