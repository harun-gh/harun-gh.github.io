<script lang="ts">
    import GithubIcon from "$lib/assets/github.svg";
    import CodebergIcon from "$lib/assets/codeberg.svg";
    import XIcon from "$lib/assets/x.svg";
    import SnsLinks from "./sns-links.svelte";
</script>

<main>
    <section class="avatar">
        <img alt="Harutoのアイコン" src="/favicon.webp" />
    </section>

    <section class="intro">
        <h2 class="realname">Haruto Nakamura</h2>
        <ul>
            <li>新大学1年生</li>
            <li>プログラミング初心者</li>
        </ul>
    </section>

    <section class="sns-links">
        <SnsLinks
            props={[
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
            ]}
        />
    </section>
</main>

<style>
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
                object-fit: cover;
                box-shadow: 15px 15px 30px rgba(0, 0, 0, 0.15);
                transform: rotate(-8deg);
                width: 240px;
                height: 240px;
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