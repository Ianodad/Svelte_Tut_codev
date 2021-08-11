<script>
    import { onMount } from 'svelte'
    import Username from './Username.svelte'
    let posts = []

    onMount (async()=>{
        const response = await fetch('https://jsonplaceholder.typicode.com/posts')
        posts = await response.json()
        console.log(posts)
    })
</script>


{#each posts as post (post.id)}
		<h2>{post.id}. {post.title}</h2>
        <p>{post.body}</p>
        <hr/>
        {:else}
        <p>loading...</p>
        <!-- <Username id={post.userId}/> -->
        <!-- <p>{post.userId}<p> -->
{/each}