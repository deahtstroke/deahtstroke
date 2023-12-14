<script context="module">
    import NavBar from "../lib/components/nav-bar.svelte";

    let showOptions = false;
    let screenWidth = 0;

    export function init() {
        screenWidth = window.innerWidth;
        window.addEventListener("resize", handleResize);
        return () => {
            window.removeEventListener("resize", handleResize);
        };
    }

    export async function load({ page }) {
        return { showOptions, screenWidth, page };
    }

    const toggleOptions = () => {
        showOptions = !showOptions;
    };

    const handleResize = () => {
        screenWidth = window.innerWidth;
    };
</script>

<NavBar />

<slot />

<style>
    @import url("/src/global.css");
</style>
