<script>
    import Icon from "./Icon.svelte";
</script>

<div class="search-bar">
    <span class="search-bar__icon search-bar__icon--search">
        <Icon name="search" fill="currentColor" />
    </span>

    <input class="search-bar__input" type="text" />

    <span class="search-bar__icon--voice">
        <Icon name="microphone"/>
    </span>
</div>

<style>
    .search-bar {
        margin-top: 0.5rem;
        width: 34rem;
        padding: 0.6rem 1.2rem;
        border-radius: 3rem;
        background: #202124;
        outline: 0.5px solid #ccc6;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .search-bar:hover {
        background: #303134;
        box-shadow: 0 0 0.4rem #0006;
        outline: none;
    }
    .search-bar__input {
        margin-left: 0.5rem;
        background: none;
        border: none;
        outline: none;
        width: 100%;
        color: #e8eaed;
        font-size: 1rem;
        font-weight: 500;
    }
    .search-bar__icon {
        display: flex;
        align-items: center;
        height: 100%;
    }
    .search-bar__icon--search {
        width: 1.5rem;
        height: 1.5rem;
        color: #9aa0a6;
    }
    .search-bar__icon--voice {
        height: 1.8rem;
        width: 1.8rem;
    }
</style>
