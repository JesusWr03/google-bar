<script>
    import Icon from "./Icon.svelte";

    let visible = false;

    function click() {
        visible = !visible;
    }
</script>

<header class="header">
    <nav class="navbar">
        <ul class="navbar__links">
            <li>About</li>
            <li>Store</li>
        </ul>

        <ul class="navbar__links">
            <li>Gmail</li>
            <li>Images</li>
            <li on:click={click} class="navbar__links__menu">
                <Icon name="menu" fill="currentColor" />

                {#if visible}
                    <div class="menu-options">
                    <ul>
                        <li>
                            <a href="#e"> Link </a>
                        </li>
                        <li>
                            <a href="#e"> Link </a>
                        </li>
                        <li>
                            <a href="#e"> Link </a>
                        </li>
                    </ul>
                    </div>
                {/if}
            </li>
            <li class="navbar__links__profile">
                <img
                    src="https://images.unsplash.com/photo-1481437642641-2f0ae875f836?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80"
                    alt="beautiful landscape"
                />
            </li>
        </ul>
    </nav>
</header>

<style>
    .header {
        padding-inline: 1em;
        width: 100%;
    }
    .header .navbar {
        display: flex;
        justify-content: space-between;
    }
    .header .navbar__links {
        padding: 0;
        display: flex;
        align-items: center;
        gap: 1.4rem;
        list-style: none;
        color: #fff;
        font-size: 0.95rem;
    }
    .header .navbar__links:first-of-type {
        color: #bdc1c6;
    }
    .header .navbar__links__menu {
        cursor: pointer;
        color: rgba(255, 255, 255, 0.87);
        height: 1.7rem;
        width: 1.7rem;
        position: relative;
    }

    .menu-options {
        position: absolute;
        top: 0;
        left: -10rem;
        background: rgb(53, 53, 53);
        width: 6rem;
        padding-block: 0.5rem;
        border-radius: 0.5rem;
    }
    .menu-options ul {
        list-style: none;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 1rem;
    }
    .menu-options ul a {
        color: #fff;
        text-decoration: none;
    }

    .header .navbar__links__profile img {
        width: 2.3rem;
        border-radius: 50%;
        aspect-ratio: 1/1;
    }
</style>
