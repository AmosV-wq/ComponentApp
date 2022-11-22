<div class="loader">
    <div class="item left" />
    <div class="item" />
    <div class="item right" />
</div>

<style>
    .loader {
        width: 550px;
        height: 200px;
        display: flex;
        align-items: center;
        justify-content: center;
        filter: blur(7px) contrast(20);
    }

    .item {
        position: relative;
        left: 15px;
        width: 55px;
        height: 55px;
        border-radius: 100%;
        background-color: #0e4961;
        box-shadow: 0 0 20px #00fff8;
    }

    .item:nth-child(2n) {
        animation: pulse 2.2s ease-in-out 1.1s infinite;
    }

    @keyframes pulse {
        50% {
            transform: scale(1.8);
        }
        70% {
            transform: scale(0.8);
        }
    }

    .left {
        transform: translate(55px);
        animation: shootLeft 2.2s ease-in-out 0.2s infinite;
    }
    .right {
        transform: translate(-55px);

        animation: shootRight 2.2s ease-in-out 0.2s infinite;
    }

    @keyframes shootLeft {
        40% {
            transform: translate(55px);
        }
        90% {
            transform: translateX(-50px);
        }
    }

    @keyframes shootRight {
        40% {
            transform: translate(-55px);
        }
        90% {
            transform: translateX(50px);
        }
    }
</style>
