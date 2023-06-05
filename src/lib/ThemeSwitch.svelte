<script lang="ts">
    import {theme} from "../stores";

    function toggle() {
        theme.update(old => old === "light" ? "dark" : "light");
    }
</script>

<button on:click={toggle}>
    <slot />
</button>