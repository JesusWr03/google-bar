<script>
    import Header from "./lib/Header.svelte";
    import SearchBar from "./lib/SearchBar.svelte";

    // console.log(Header.name);

    // function clickEvent(){
    //    bool = !bool
    // }
</script>

<main>
    <Header />
    <div>
        <figure>
            <img
                src="https://www.google.com/images/branding/googlelogo/1x/googlelogo_light_color_272x92dp.png"
                alt=""
            />
        </figure>
        <SearchBar />
    </div>
</main>

<style>
    main {
        min-height: 100vh;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    div {
        display: flex;
        flex-direction: column;
        align-items: center;
        max-width: 1280px;
    }
</style>
