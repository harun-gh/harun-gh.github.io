<script>
    import MainVisual from "$lib/components/main-visual.svelte";
    import { FileBraces, LibraryBig, Link, Music4, Users } from "@lucide/svelte";
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

    <section class="belong-circles">
        <h2><Users /> 所属サークル</h2>

        <ul>
            <li>ソフトメディア研究会 P班</li>
            <li>ネットワークコンテンツ研究会</li>
            <li>第二テニスサークル</li>
        </ul>
    </section>

    <section class="skills">
        <h2><FileBraces /> 扱えるプログラミング言語</h2>

        <ul>
            <li>Zig</li>
            <li>TypeScript(+ JavaScript)</li>
            <li>HTML</li>
            <li>CSS</li>
            <li>Assembly (x86_64 命令アーキテクチャ)</li>
        </ul>
    </section>

    <section class="favorite-works">
        <h2><LibraryBig /> 好きな作品</h2>

        <ul>
            <li>狼と香辛料 <small>(アニメ, 漫画, 小説)</small></li>
            <li>狼と羊皮紙 <small>(小説)</small></li>
            <li>とんがり帽子のアトリエ <small>(アニメ, 漫画)</small></li>
            <li>メイドインアビス <small>(アニメ, 映画, 漫画)</small></li>
            <li>Unnamed Memory <small>(小説)</small></li>
            <li>葬送のフリーレン <small>(漫画)</small></li>
            <li>NieR:Automata <small>(ゲーム)</small></li>
            <li>サマータイムレンダ <small>(アニメ, 漫画)</small></li>
            <li>夜は猫といっしょ <small>(漫画)</small></li>
        </ul>
    </section>

    <section class="favorite-music">
        <h2><Music4 /> 好きな音楽</h2>

        <iframe title="Haruto's Playlist on Spotify" data-testid="embed-iframe" style="border-radius:12px" src="https://open.spotify.com/embed/playlist/3pfYptaerXN1Sw6p1rl8nZ?utm_source=generator" width="100%" height="352" frameBorder="0" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
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