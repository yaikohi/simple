<script lang="ts">
    export let src: string;
    export let desc: string;
</script>

<img src={src} alt={desc} />

<style>
	img {
		height: 14rem;
		width: auto;
    }
</style>