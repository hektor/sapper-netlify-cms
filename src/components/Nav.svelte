<script>
  export let segment;
</script>

<style>
  nav {
    display: flex;
    border-bottom: 1px solid #eee;
  }

  [aria-current] {
    border-bottom: 1px solid #000;
  }

  a {
    padding: 0.8rem;
  }
</style>

<nav>
  <a aria-current={segment === undefined ? 'page' : undefined} href=".">Home</a>
  <a aria-current={segment === 'about' ? 'page' : undefined} href="about">
    About
  </a>
  <!-- rel=prefetch prefetches on hover or tap -->
  <a
    rel="prefetch"
    aria-current={segment === 'blog' ? 'page' : undefined}
    href="blog">
    Blog
  </a>
</nav>
