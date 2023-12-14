<script>
    export let options;

    let showOptions = false;

    const toggleOptions = () => {
        showOptions = !showOptions;
    };

    const handleKeyDown = (event) => {
        if(event.key == 'Enter' || event.key === ' ') {
            toggleOptions();
        }
    }
</script>

<div class="burger-menu" on:click={() => toggleOptions()} on:keydown={() => handleKeyDown()} role="button" tabindex=0>
    <span class="material-symbols-outlined">menu</span>
    {#if showOptions}
        {#each options as option}
            <div class="burger-option">{option}</div>
        {/each}
    {/if}
</div>

<style>
    @import url("/src/global.css");
    .burger-menu {
        display: block;
        cursor: pointer;
    }
    .burger-menu .burger-option {
        display: none;
        padding: 10px;
        border-bottom: 1px solid var(--light-color);
    }
    .burger-menu:hover .burger-option {
        display: block;
    }
</style>
