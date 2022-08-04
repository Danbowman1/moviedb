<script context="module">
    export async function load({ fetch }){
        const res = await fetch(`https://api.themoviedb.org/3/movie/popular?api_key=9640f699ceb8be11e7f1bc51d66a7c64&language=en-US&page=1`);
        const data = await res.json();
        if(res.ok){
            return {
                props: { popular: data.results }
            }
        }
    }
</script>

<script>
    import PopularMovies from '../components/PopularMovies.svelte'
    import SearchMovies from '../components/SearchMovies.svelte';
    export let popular;
    
</script>

<main>
    <SearchMovies />
    <PopularMovies {popular}/>
</main>