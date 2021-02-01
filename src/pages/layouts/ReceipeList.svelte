<script lang="ts">
    import resep from '../../dummy/Resep'
    import { favorites, filter } from '../../store';

</script>

<div class="pt-5">
    <p class="text-xl font-bold text-center">Hasil Pencarian Resep</p>
    <div class="flex items-center justify-center">
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 pt-5">
            {#each resep as r}
                    
                {#if r.name.includes($filter)}
                    <div class="rounded-lg m-2" id="card">
                        <img src={r.image_url} alt="" class="rounded">
                        <div class="flex items-center justify-between py-2 px-3">
                            <p class="font-bold text-sm">{r.name}</p>
                            <button
                                on:click={() => {
                                    const data = JSON.parse($favorites)
                                    data.push(r)
                                    favorites.set(JSON.stringify(data))
                                }} 
                                class="font-bold text-sm p-2 rounded-xl">
                                favorit
                            </button>
                        </div>
                    </div>
                {:else if r.name === ""}
                    <div class="rounded-lg m-2" id="card">
                        <img src={r.image_url} alt="" class="rounded">
                        <div class="flex items-center justify-between py-2 px-3">
                            <p class="font-bold text-sm">{r.name}</p>
                            <button
                                on:click={() => {
                                    const data = JSON.parse($favorites)
                                    data.push(r)
                                    favorites.set(JSON.stringify(data))
                                }}
                                class="font-bold text-sm p-2 rounded-xl">
                                favorit
                            </button>
                        </div>
                    </div>
                {/if}
                
            {/each}
            
        </div>
    </div>
</div>

<style>
    p{
        color: #9CCD62;
        font-family: Raleway;
    }
    button{
        background-color: #9CCD62;
        font-family: Raleway;
    }
    #card{
        background-color: #3A3C42;
    }
</style>