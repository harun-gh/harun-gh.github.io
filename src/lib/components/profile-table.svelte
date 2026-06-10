<script lang="ts">
    interface Props {
        contents: {
            [key: string]: string;
        }
    }

    const { contents }: Props = $props();
</script>

<div>
    <p>自己紹介</p>

    <table>
        <tbody>
            {#each Object.entries(contents) as [key, value]}
                <tr>
                    <th>{key}</th>
                    <td>{value}</td>
                </tr>
            {/each}
        </tbody>
    </table>
</div>

<style>
    div {
        width: clamp(320px, 90vw, 900px);
        margin: 1.5rem 0;
    }

    p {
        margin-bottom: 1rem;
        font-size: .8rem;
        letter-spacing: .2em;
        text-transform: uppercase;
    }

    table {
        width: 100%;
        border-collapse: collapse;

        & tr {
            width: 100%;
            border-bottom: 1px dotted rgb(255, 255, 255);

            &:first-child {
                border-top: 1px dotted rgb(255, 255, 255);
            }
        }

        & th {
            width: 12rem;
        }

        & td {
            font-weight: 500;
        }

        & th, & td {
            padding: 1rem 0;
            text-align: left;
        }
    }
</style>