<script lang="ts">
    interface Prop {
        service_name: string;
        href: string;
        image_src: string;
        title: string;
    }

    interface Props {
        props: Prop[]
    }

    const { props }: Props = $props();
</script>

<ul>
    {#each props as { href, image_src, service_name, title }}
        <li>
            <a {href} {title}>
                <img src={image_src} alt={`${service_name} のロゴ`} />
            </a>
        </li>
    {/each}
</ul>

<style>
    ul {
        list-style: none;
        display: flex;
        gap: 1rem;
        
        li {
            opacity: 0.8;
        }

        li:hover {
            opacity: 1;
        }

        li img {
            object-fit: contain;
            width: 3rem;
            height: 3rem;
        }
    }
</style>