<template>
  <nav class="container">
    <header>
      <a target="_blank" rel="noopener noreferrer" className="nav-a" href="https://www.adithyabhat.com/">
        <img src="https://www.adithyabhat.com/static/media/adithya1.a0fbc905.png" class="back" alt="logo"/>
      </a>
    </header>
  </nav>
</template>

<script>

    export default {
        name: 'Nav'
    }

</script>

<style>
    nav > header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-top: 20px;
    }
    .back {
      width: 60px !important;
    }
    .home {
      color: #444;
      margin-top: 5px;
    }
</style>