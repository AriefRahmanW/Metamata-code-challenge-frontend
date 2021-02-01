<script>
    import Navbar from './layouts/AppBar.svelte';
    import Banner from './layouts/Banner.svelte';
    import Footer from './layouts/Footer.svelte';
    import ReceipeList from './layouts/ReceipeList.svelte';
    import Search from './layouts/Search.svelte';
</script>

<Navbar/>

<div class="container mx-auto px-10">
    <Banner/>
    <Search/>
    <ReceipeList/>
</div>

<Footer/>