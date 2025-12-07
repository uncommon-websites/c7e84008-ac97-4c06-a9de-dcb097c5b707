<script lang="ts">
	import "../app.css";
    import Header from "$lib/components/Header.svelte";
    import Footer from "$lib/components/Footer.svelte";
</script>

<div class="min-h-screen bg-white font-sans text-gray-900 selection:bg-orange-100 selection:text-orange-900">
    <Header />
    <slot />
    <Footer />
</div>
