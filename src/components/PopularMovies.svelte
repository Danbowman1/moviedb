<script>
    export let popular
    
</script>

<h3>Popular Movies</h3>
<div class="popular-movies">
    <div class="movie"></div>
    {#each popular as movie}
        <h1>{movie}</h1>
    {/each}
</div>

