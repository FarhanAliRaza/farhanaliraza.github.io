
    <!-- src/routes/+page.svelte -->

    <script lang="ts">
        import type { PageServerData } from './$types';

        export let data: PageServerData;

        console.log(data, "data");
    </script>

    <div class="container">
        <h1>Markdown Blog</h1>

        <ul class="links">
            {#each data.posts as post}
            <li>
                <a href={`/post/${post.slug}`}>{post.title}</a>
            </li>
            {/each}
        </ul>
    </div>

    <style>
      
    </style>

