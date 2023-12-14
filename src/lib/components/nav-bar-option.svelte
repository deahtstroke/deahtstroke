<script>
    export let href = "#"; // default value
    export let iconName = "";
    export let buttonText = ""; //default value
</script>

<div class="nav-bar-item">
    <a {href}>
        <span class="material-symbols-outlined"> {iconName} </span>
        {buttonText}
    </a>
</div>

<style>
    @import url("/src/global.css");
    .nav-bar-item {
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        padding: 1px;
    }
    .nav-bar-item a {
        display: flex;
        align-items: center;
        justify-content: center;
        text-decoration: none;
        box-sizing: border-box;
        gap: 0.25rem;
        width: 100px;
        height: 33px;
        color: var(--light-color);
        font-size: 15px;
        position: relative;
    }
    .nav-bar-item a:hover {
        background-color: var(--background-hover-color);
        border-radius: 4px;
        transition: all 0.3s ease;
    }
</style>
