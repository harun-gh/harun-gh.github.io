<script>
    import MainVisual from "$lib/components/main-visual.svelte";
    import { FileBraces, Link } from "@lucide/svelte";
</script>

<MainVisual />

<section class="content">
    <section class="links">
        <h2><Link /> リンク</h2>

        <ul>
            <li><a href="https://github.com/harun-gh" rel="author" target="_blank">Github: @harun-gh</a></li>
            <li><a href="https://x.com/haruto1521" rel="author" target="_blank">Twitter: @haruto1521</a></li>
            <li><a href="https://discordapp.com/users/1489466214450331760" rel="author" target="_blank">Discord: haruto_1521</a></li>
        </ul>
    </section>

    <section class="skills">
        <h2><FileBraces /> できるプログラミング言語</h2>

        <ul>
            <li>Zig 0.15.2 / 0.16.0</li>
            <li>TypeScript(+ JavaScript)</li>
            <li>HTML</li>
            <li>CSS</li>
        </ul>
    </section>

</section>

<style>
    section.content {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0 10vw;
        flex-direction: column;

        & > * {
            width: clamp(320px, 75vw, 750px);
        }
    }
</style>