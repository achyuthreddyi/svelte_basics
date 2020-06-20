<script>
    import { onMount } from 'svelte'
    const apiBaseUrl = 'https://www.youtube.com/redirect?redir_token=3YcJoeUmP33G1WrEFzz3z5J-vSd8MTU5MjcxNjYxOEAxNTkyNjMwMjE4&event=video_description&v=vhGiGqZ78Rs&q=https%3A%2F%2Fndb99xkpdk.execute-api.eu-west-2.amazonaws.com%2Fdev/posts'
    let posts = [];
    onMount(async() =>{
        const res = await fetch(apiBaseUrl)
        posts = await res.json()
        console.log(posts);
        
    })
 </script>

<div class="row">
    {#if posts.length === 0}
        <h3> loading posts ......</h3>
    {:else}
        {#each posts as post}
            <div class="col s6">
                <div class="card">
                <div class="card-content">
                    <p class="card-title">{post.title}</p>
                    <p>{post.createdAt}</p>
                    <p>{post.body}</p>
                </div></div>
            </div>
            {/each}
            {/if}

</div>