<script lang="ts">
    import GithubIcon from "$lib/assets/github.svg";
    import CodebergIcon from "$lib/assets/codeberg.svg";
    import XIcon from "$lib/assets/x.svg";
    import SnsLinks from "./sns-links.svelte";

    // import { Tween } from 'svelte/motion';
    // import { cubicOut } from 'svelte/easing';
    import { Zap } from "@lucide/svelte";

    const links = [
        {
            service_name: "Github",
            image_src: GithubIcon,
            href: "https://github.com/harun-gh",
            title: "Github: @harun-gh"
        },
        {
            service_name: "Codeberg",
            image_src: CodebergIcon,
            href: "https://codeberg.org/haruto_n",
            title: "Codeberg: @haruto_n"
        },
        {
            service_name: "X (Twitter)",
            image_src: XIcon,
            href: "https://x.com/haruto1521",
            title: "X (Twitter): @haruto1521"
        }
    ];

    // const animation = new Tween(0, {
    //     duration: 500,
    //     easing: cubicOut
    // });

    // $effect(() => {
    //     animation.target = -10;
    // });
</script>

<main>
    <section class="avatar">
        <img
            alt="Harutoのアイコン"
            src="/favicon.webp"
            // style="transform: rotate({animation.current}deg);"
        />
    </section>

    <section class="intro">
        <h2 class="realname">Haruto Nakamura</h2>
        <ul>
            <li>新大学1年生 / 低レイヤーにハマってます</li>
            <li>主に <span class="zig"><Zap /> Zig</span> で開発してます</li>
        </ul>
    </section>

    <section class="sns-links">
        <SnsLinks props={links} />
    </section>
</main>

<style>
    .zig {
        color: #FFC20E;
    }

    main {
        width: 100vw;
        height: 100vh;
        display: flex;
        position: relative;
        align-items: center;
        justify-content: center;

        & section.avatar {
            flex: 1;
            display: flex;
            align-items: center;
            justify-content: center;

            & img {
                transition: box-shadow .3s ease, scale .3s ease, transform .3s ease;
                object-fit: cover;
                box-shadow: 15px 15px 30px rgba(0, 0, 0, 0.15);
                width: 240px;
                height: 240px;
                transform: rotate(-10deg);

                --scale-on-hover: 1.1;

                &:hover {
                    box-shadow: 25px 25px 50px rgba(0, 0, 0, 0.2);
                    transform: rotate(-4deg) scale(var(--scale-on-hover));
                }

                &:hover:active {
                    transform: rotate(-4deg) scale(calc(var(--scale-on-hover) * 0.92));
                }
            }
        }

        & section.intro {
            flex: 1;

            & h2.realname {
                font-size: 3rem;
                -webkit-text-stroke: 2px #333;
                color: transparent;
                margin: 2rem 0;
            }

            & ul {
                list-style: none;
            }

            & ul li {
                font-size: 1.25rem;
                line-height: 1.8;

                &::before {
                    content: "○";
                    margin-right: 1.5rem;
                    font-size: 0.7em;
                    color: #000000;
                    vertical-align: middle;
                }
            }
        }

        & section.sns-links {
            position: absolute;
            top: auto;
            left: auto;
            bottom: 5vh;
            right: 5vw;
        }
    }
</style>