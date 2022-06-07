<template>
  <header class="header__inner">
    <div class="container">
      <div class="header__logo">
        <img src="../../assets/img/spotify-logo.png">
      </div>
    </div>
  </header>
</template>

<script>
export default {
    name: 'BaseHeader',
}
</script>

<style lang="scss" scoped>
.header__inner{
    background-color: var(--background__header__color);
}
.header__logo {
    width: 100%;
    height: 10vh;
    display: flex;
    justify-content: start;
    align-items: center;
    
    
  
    img{
    max-width: 100%;
    max-height: 7vh;
  }
}
</style>