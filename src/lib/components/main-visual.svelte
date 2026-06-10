<script lang="ts">
    import { Zap } from "@lucide/svelte";
    import ScrollPrompt from "./scroll-prompt.svelte";
    import WaveBackground from "./wave-background.svelte";

    import GithubLogo from "../assets/github.svg";
    import TwitterLogo from "../assets/x.svg";
    import DiscordLogo from "../assets/discord.svg";
</script>

<section class="main-visual">
    <WaveBackground />

    <div class="boundary">
        <img class="avatar" src="/favicon.webp" alt="Harutoのアイコン">
        
        <div class="introduce">
            <h1>Haruto Nakamura</h1>
            <div class="divider"></div>
            <p class="pronoun">主に <span class="zig"><Zap /> Zig</span> で開発しています</p>

            <ul class="socials">
                <li><a href="https://github.com/harun-gh" rel="author" target="_blank">Github <img src={GithubLogo} alt="GitHub's Logo"></a></li>
                <li><a href="https://x.com/haruto1521" rel="author" target="_blank">Twitter <img src={TwitterLogo} alt="Twitter's Logo"></a></li>
                <li><a href="https://discordapp.com/users/1489466214450331760" rel="author" target="_blank">Discord <img src={DiscordLogo} alt="Discord's Logo"></a></li>
            </ul>
        </div>
    </div>
</section>

<ScrollPrompt />

<style>
    section.main-visual {
        background: #fff;
        color: #474747;
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

    .introduce {
        & h1 {
            -webkit-text-stroke: 1.5px #474747;
            color: transparent;
        }

        & .divider {
            width: 4rem;
            height: .125rem;
            background: #474747;
            margin-top: 1rem;
            margin-bottom: .5rem;

            @media (max-width: 48rem) {
                margin-top: .5rem;
                margin-left: auto;
                margin-right: auto;
            }
        }

        & .pronoun {
            color: #000;
            font-weight: 300;
            line-height: 2rem;
        }

        & .socials {
            margin: 1rem 0;
            list-style: none;
            display: flex;
            gap: 1rem;

            & li {
                border: solid 2.5px #474747;
                padding: .25rem 1rem;
                border-radius: 1rem;
                font-size: smaller;
                transition: all .1s;

                & a {
                    display: flex;
                    gap: .5rem;
                    justify-content: center;
                    align-items: center;
                }

                & img {
                    width: 1rem;
                    height: 1rem;
                }
            }
        }
    }

    .zig {
        color: rgb(214, 158, 0);
        font-weight: 400;
    }
</style>