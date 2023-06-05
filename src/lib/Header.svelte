<script>
    import ThemeSwitch from "$lib/ThemeSwitch.svelte";
</script>

<header class="header">
    <nav class="nav">
        <section>
            <h2>Name</h2>
        </section>
        <section>

        </section>
        <section style="display: flex; align-items: center; gap: 6px;">
            <button>Log In</button>
        </section>
    </nav>
</header>

<style>
    .header {
        width: 100%;
        backdrop-filter: blur(4px);
    }
    .nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin: 30px 0px;
    }
</style>
