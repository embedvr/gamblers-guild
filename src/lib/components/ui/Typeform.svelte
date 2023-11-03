<script lang="ts">
    let form: HTMLDivElement;
    import { createWidget } from "@typeform/embed";
    import "@typeform/embed/build/css/widget.css";
    import { onMount } from "svelte";

    onMount(() => {
        createWidget("p5LtH4lD", {
            container: form,
        });
    });
</script>

<div bind:this={form} style="width: 100%; height: 500px;" />
