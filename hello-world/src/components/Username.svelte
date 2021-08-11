<script>
import {onMount} from 'svelte'

let userName = ''
export let id 
onMount(async()=>{
    
    const response = await fetch(`https://jsonplaceholder.typicode.com/posts?userId=${id}`)
        userName = await response.json()
        console.log(userName)
})
</script>

<p>{userName}</p>