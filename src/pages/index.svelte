<script>
    import Navbar from './_components/AppBar.svelte';
    import Banner from './_components/Banner.svelte';
    import Footer from './_components/Footer.svelte';
    import ReceipeList from './_components/ReceipeList.svelte';
    import Search from './_components/Search.svelte';
</script>

<Navbar/>

<div class="container mx-auto px-10">
    <Banner/>
    <Search/>
    <ReceipeList/>
</div>

<Footer/>