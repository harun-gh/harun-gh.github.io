<!-- クレジット: https://junpei-sugiyama.com/scroll-down/#:~:text=100%25%3B%20%7D%20%7D-,%E7%9F%A2%E5%8D%B0 -->

<div class="scroll">
  <span></span>
</div>

<style>
    .scroll {
        padding-top: 60px;
        position: absolute;
        text-align: center;
        left: 50%;
        bottom: 10vh;
    }
    .scroll::before {
        animation: scroll 1.5s infinite;
        border-bottom: 2px solid #000;
        border-left: 2px solid #000;
        content: "";
        height: 20px;
        left: 0;
        margin: auto;
        position: absolute;
        right: 0;
        top: 0;
        width: 20px;
    }
    @keyframes scroll {
        0% {
            opacity: 0;
            transform: rotate(-45deg) translate(0, 0);
        }
        40% {
            opacity: 1;
        }
        80% {
            opacity: 0;
            transform: rotate(-45deg) translate(-20px, 20px);
        }
        100% {
            opacity: 0;
        }
    }
</style>