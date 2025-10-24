<script lang="ts">
    let { nimi } = $props();
    let arvo = $state("rasse");
</script>

<h1>minun nimeni on {arvo}</h1>

<input type="text" bind:value={arvo} />
