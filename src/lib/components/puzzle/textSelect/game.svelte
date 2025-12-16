<script lang="ts">
    import type { GameInput, GameOutput } from "./index"
    import { onMount } from "svelte"

    let { data, setSubmitable }: { data: GameInput, setSubmitable: () => void } = $props()

    const output: GameOutput = {}
    export function getSubmitData(): GameOutput {
        return output
    }

    export function getSubmitScore(): number {
        return 0
    }

    onMount((): void => {
        setSubmitable()
    })
</script>
