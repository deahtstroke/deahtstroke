<script>
    import NavBarOption from "./nav-bar-option.svelte";
    import NavBarBurger from "./nav-bar-burger.svelte";

    let showOptions = false;
    let screenWidth = 0;

    let burgerOptions = ["Projects", "Contact", "Resume"];

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

<div class="nav-bar">
    <h3>Daniel Villavicencio</h3>
    {#if screenWidth >= 600}
        <NavBarOption href="/" iconName="home" buttonText="Home" />
        <NavBarOption
            href="/projects"
            iconName="description"
            buttonText="Projects"
        />
        <NavBarOption
            href="/contact"
            iconName="person_book"
            buttonText="Contact"
        />
        <NavBarOption
            href="/resume"
            iconName="description"
            buttonText="Resume"
        />
    {:else}
        <NavBarBurger options={burgerOptions} />
    {/if}
</div>

<style>
    @import url("/src/global.css");
    .nav-bar {
        background-color: var(--nav-background-color);
        margin-bottom: 1.5rem;
        gap: 1.8rem;
        padding: 10px;
        height: 40px;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    @media screen and (min-width: 600px) {
        .nav-bar {
            background-color: var(--nav-background-color);
            margin-bottom: 1.5rem;
            gap: 1.8rem;
            padding: 10px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
    }
</style>
