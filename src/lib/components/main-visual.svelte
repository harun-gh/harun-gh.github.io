<script lang="ts">
    import { Zap } from "@lucide/svelte";
    import ScrollPrompt from "./scroll-prompt.svelte";
</script>

<section class="main-visual">
    <div class="boundary">
        <img class="avatar" src="/favicon.webp" alt="Harutoのアイコン">
        
        <div class="introduce">
            <h1>Haruto Nakamura</h1>

            <ul>
                <li>新大学1年生 / 低レイヤーにハマってます</li>
                <li>主に <span class="zig"><Zap /> Zig</span> で開発してます</li>
            </ul>
        </div>
    </div>
</section>

<ScrollPrompt />

<style>
    section.main-visual {
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
    }

    .boundary {
        display: flex;
        align-items: center;
        gap: clamp(1.5rem, 10vw, 10rem);

        @media (max-width: 48rem) {
            flex-direction: column;
            text-align: center;
        }
    }

    .avatar {
        --image-size: clamp(170px, 18vw, 240px);
        height: var(--image-size);
        width: var(--image-size);
        object-fit: cover;
        flex-shrink: 0;
        transition: box-shadow .3s ease, scale .3s ease, transform .3s ease;
        box-shadow: 15px 15px 30px rgba(0, 0, 0, 0.15);
        transform: rotate(-5deg);

        --scale-on-hover: 1.1;

        &:hover {
            box-shadow: 25px 25px 50px rgba(0, 0, 0, 0.2);
            transform: rotate(0deg) scale(var(--scale-on-hover));
        }

        &:hover:active {
            transform: rotate(0deg) scale(calc(var(--scale-on-hover) * 0.92));
        }
    }

    .introduce h1 {
        -webkit-text-stroke: 2px #333;
        color: transparent;
        margin: 2rem 0;
    }

    .zig {
        color: rgb(214, 158, 0);

        & > :global(svg) {
            vertical-align: middle;
        }
    }
</style>