<template>
  <body>
    <div class="grid-wrapper">
      <header> header </header>
      <nav> nav </nav>
      <section> section </section>
      <main>
        <article>  </article>
        <article>  </article>
        <article>  </article>
        <article>  </article>
        <article>  </article>
        <article>  </article>
      </main>

      <footer> footer </footer>
    </div>
  </body>
</template>

<script>
</script>

<style>

.grid-wrapper {
    display:  grid;
    grid-template-rows: repeat(4, auto);    
    grid-template-columns: 240px 1fr;
    gap:  1rem;
  }
  
  .grid-wrapper>* {
    min-height: 100px;
    border-radius: 2px;

    display: flex;
    justify-content: center;
    align-items: center;
  }

  .grid-wrapper>main {
    background-color: rgb(92, 92, 92);
    display: grid;
    grid-auto-rows: auto;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
  }

  header {
    background-color: rgb(92, 92, 92);
    grid-column: 1 / -1;
    grid-row: 1;
  } 
    
  nav {
    background-color: rgb(92, 92, 92);
    grid-row: 2 / -2;
  }
     
  section {
    background-color: rgb(92, 92, 92);
    grid-column: 2 / -1;
  } 

  article {
    background-color: rgb(107, 107, 107);
    min-height: 100px;
  } 

  footer {
    background-color: rgb(92, 92, 92);
    grid-column: 1 / -1;
  }

</style>
