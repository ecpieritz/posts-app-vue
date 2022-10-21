<template>
  <header class="d-flex flex-lg-row flex-sm-column justify-content-between align-items-center">
    <div class="header__title">
      <h1>Posts App</h1>
      <p>Made with 💙 by Emilyn Pieritz</p>
    </div>
    <div class="header__socials d-flex flex-row">
      <a class="header__socials__link" href="https://github.com/ecpieritz" target="_blank" rel="noopener noreferrer">
        <img src="https://github.com/ecpieritz/png-logos/blob/main/github-white.png?raw=true" alt="github">
      </a>
      <a class="header__socials__link" href="https://www.linkedin.com/in/ecpieritz/" target="_blank" rel="noopener noreferrer">
        <img src="https://github.com/ecpieritz/png-logos/blob/main/linkedin-white.png?raw=true" alt="linkedin">
      </a>
    </div>
  </header>
</template>

<script>
export default {
  name: 'header-app'
}
</script>

<style scoped>
  header{
    background-color: var(--dark-blue);
    color: var(--white);
    padding: 30px 60px;
  }
  
  .header__socials{
    gap: 20px;
  }

  .header__socials__link img{
    width: 40px;
  }

  @media(max-width: 960px){
    header{
      padding: 15px 60px;
    }

    .header__title{
      text-align: center;
      margin-bottom: 10px;
    }
  }
</style>
