<script>
    import MainVisual from "#lib/components/main-visual.svelte";
    import ProfileTable from "#lib/components/profile-table.svelte";
    import { SixteenthNotes } from "@lucide/svelte";
    import "../globals.css";
</script>

<MainVisual />

<section class="content">
    <section class="about-me">
        <h2>私について</h2>

        <p>
            大学一年生(2026/04入学)で、低レイヤーとWeb開発が好きです
        </p>

        <ProfileTable contents={{
            "学部/学科": "情報変革科学部 認知情報科学科",
            "学年": "1年生 (1回生, 2026/04入学)",
            "サークル": "ソフトメディア研究会, ネットワークコンテンツ研究会, 第2テニスサークル",
            "バイト": "やってません",
            "主な言語": "Zig, HTML, CSS, TypeScript(+ JavaScript)"
        }} />
    </section>

    <section class="favorite-music">
        <h2><SixteenthNotes /> 好きな音楽</h2>

        <iframe title="Haruto's Playlist on Spotify" data-testid="embed-iframe" style="border-radius:12px" src="https://open.spotify.com/embed/playlist/3pfYptaerXN1Sw6p1rl8nZ?utm_source=generator" width="100%" height="352" frameBorder="0" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
    </section>

</section>

<style>
    section.content {
        color: #fff;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0 10vw;
        flex-direction: column;
        & > section {
            width: clamp(320px, 75vw, 750px);
        }
    }

    h2 {
        margin: 1.5rem 0;
    }

    p {
        margin: .5rem 0;
    }
</style>