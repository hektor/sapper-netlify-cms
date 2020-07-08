<script context="module">
  export function preload({ params, query }) {
    return this.fetch(`blog.json`)
      .then(r => r.json())
      .then(posts => {
        return { posts };
      });
  }
</script>

<script>
  export let posts;
</script>

<h1>Recent posts</h1>
{#each posts as post}
  <!-- prefetch loads data on hover or tap -->
  <a rel="prefetch" href="blog/{post.slug}">{post.title}</a>
{/each}

