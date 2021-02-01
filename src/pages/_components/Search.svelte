
<script lang="ts">
    import { filter } from "../../store";

</script>

<div class="flex items-center justify-center pt-5 px-14 lg:px-60 text-center">
    <div class="w-24 min-w-full">
        <input
            bind:value={$filter}
            type="text" placeholder="" class="px-3 py-2 placeholder-gray-400 text-gray-700 bg-white bg-white rounded-full text-sm border border-gray-400 outline-none focus:outline-none focus:shadow-outline w-full"/>
    </div>
    <button
        class="ml-2 px-5 py-2 placeholder-gray-400 text-white bg-white rounded-full text-sm outline-none focus:outline-none focus:shadow-outline">
        Cari
    </button>
</div>

<style>
    input{
        font-family: Raleway;
    }
    button{
        font-family: Raleway;
        background-color: #9CCD62;
    }
</style>