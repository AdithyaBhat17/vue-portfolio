<template>
  <nav>
    <header>
      <a className="nav-a" href="/">
        <img v-bind:src="back" class="back" alt="logo"/>
      </a>
      <a class="home" href="https://www.adithyabhat.com/">Home</a>
    </header>
  </nav>
</template>

<script>
    import back from '../assets/Arrow.png'

    export default {
        name: 'Nav',
        data() {
          return {
            back
          }
        }
    }

</script>

<style>
    nav > header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px;
    }
    .back {
      width: 40px !important;
    }
    .home {
      color: #444;
      margin-top: 5px;
    }
</style>