<!-- https://shanabrian.com/web/html-css-js-technics/css-wave-animation.php#:~:text=%E6%B3%A23 をベースに作成 -->

<div class="background">
    <svg viewBox="0 0 1200 300" preserveAspectRatio="none">
        <defs>
            <path
                id="wave"
                d="M0,100
                   Q150,50 300,100
                   T600,100
                   T900,100
                   T1200,100
                   V300
                   H0
                   Z"
            />
        </defs>

        <use href="#wave" class="wave1" />
        <use href="#wave" class="wave2" />
        <use href="#wave" class="wave3" />
    </svg>
</div>

<style>
.background {
    position: absolute;

    top: auto;
    left: 0;
    right: 0;
    bottom: -0.3px;

    height: clamp(150px, 30vh, 400px);

    z-index: 0;

    pointer-events: none;
    overflow: hidden;

    svg {
        width: 200%;
        height: 100%;

        use {
            fill: #2450b8;

            &.wave1 {
                opacity: 0.2;
                animation: wave 21s linear infinite reverse;
            }

            &.wave2 {
                opacity: 0.3;
                transform: translateY(10px);

                animation: wave 10s linear infinite;
            }

            &.wave3 {
                opacity: 0.15;
                transform: translateY(20px);

                animation: wave 4s linear infinite reverse;
            }
        }
    }
}

@keyframes wave {
    from {
        transform: translateX(0);
    }

    to {
        transform: translateX(-600px);
    }
}
</style>