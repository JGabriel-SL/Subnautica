<template>
    <div>
    <div class="header">
      <ul v-if="!isMobile">
        <li>Home</li>
        <li>About it</li>
      </ul>

      <div v-else class="header-mobile">
          <v-icon dark>mdi-menu</v-icon>
      </div>
    </div>

    <div>
        <img class="img" src="../assets/Union.png" width="50%"/>
      </div>

      <div :class="[isMobile ? 'logo-mobile' : 'logo']">
        <img src="../assets/logo.png" >
        <span>Lorem inpsum Lorem inpsumLorem inpsumLorem inpsumLorem inpsum Lorem inpsumLorem</span>
      </div>
    </div>
</template>

<script>
export default {
    props: { isMobile: Boolean }
}
</script>

<style>
 .header {
    position: absolute;
    right: 0;
    z-index: 1;
    padding: 20px 50px;
  }

  .header ul {
    list-style: none;
    display: flex;
  }
  .header ul li {
    cursor: pointer;
    padding: 0px 30px;
    font-weight: bold;
    font-size: 18px;
    color: white;
  }

  .header ul li:hover {
    color: orange;
    background-color: #fff;
    border-radius: 20px;
  }

  .header-mobile {
    position: absolute;
    right: 20px;
    z-index: 1;
    
  }

  .logo {
    position: absolute;
    top: 8%;
    right: 0;
    color: white;

    display: flex;
    flex-direction: column;
    align-items: center;
    width: 60%;
    text-align: center;
  }

  .logo img {
    width: 40%;
  }

  .logo span {
    width: 60%;
  }

  .logo-mobile {
    position: relative;
    top: 50px;
    margin-bottom: 50px;
    color: white;
    text-align: center;

    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
  }

  .logo-mobile img {
    width: 90%;
  }
</style>