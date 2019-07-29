<template>
  <nav class="container">
    <header>
      <a target="_blank" rel="noopener noreferrer" className="nav-a" href="https://www.adithyabhat.com/">
        <img src="https://www.adithyabhat.com/static/media/adithya1.a0fbc905.png" class="back" alt="logo"/>
      </a>
      <button :class="dark ? 'light_btn' : 'dark_btn'" v-on:click="toggleTheme">
        <span :aria-label="dark ? 'light' : 'dark'" >{{dark ? '✨' : '🌜'}}</span>
      </button>
    </header>
  </nav>
</template>

<script>

    export default {
        name: 'Nav',
        data() {
          return {
            dark: false
          }
        },
        methods: {
          toggleTheme() {
            this.dark = !this.dark
            this.dark ? 
            document.querySelector('body').classList.add('dark') :
            document.querySelector('body').classList.remove('dark')
          }
        }
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
    body.dark {
      color: #fff;
      background-color: #444;
    }
    body.dark .back {
      filter: invert(100%)
    }
    body.dark h2, body.dark p {
      color: #fff;
    }
    .light_btn, .dark_btn {
      padding: 8px 10px;
      border-radius: 5px;
      box-shadow: 5px 5px 25px 0 rgba(0, 0, 0, 0.2);
      border: none;
      outline: none !important;
    }
    .light_btn {
      background-color: #fff;
    }    
    .dark_btn {
      background-color: #444;
    }
</style>