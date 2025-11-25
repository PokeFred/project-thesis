<script lang="ts">
    import type { GameInput, GameOutput } from "./index"
    import { onMount } from "svelte"

    let { data, setSubmitable }: { data: GameInput, setSubmitable: () => void } = $props()

    const output: GameOutput = {}
    export function getSubmitData(): GameOutput {
        return output
    }

    onMount((): void => {
        setSubmitable()
    })
</script>

{#each data.informations as element}
    <div class="p-2">{element}</div>
{/each}
