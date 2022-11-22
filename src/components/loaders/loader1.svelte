<div class="loader">
    <div class="item small" />
    <div class="item" />
    <div class="item small rev" />
    <div class="item" />
    <div class="item small" />
    <div class="item" />
    <div class="item small rev" />
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

    .small {
        animation: spinLeft 4.4s linear infinite;
    }

    .rev {
        animation-direction: reverse;
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

    @keyframes spinLeft {
        from {
            transform: rotate(0deg) translate(50px);
        }
        to {
            transform: rotate(360deg) translate(50px);
        }
    }
</style>
