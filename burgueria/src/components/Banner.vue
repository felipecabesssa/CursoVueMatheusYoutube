<template>
  <div id="main-banner">
    <h2>Make Your Burger</h2>
  </div>
</template>

<script>
export default {
  name: "Banner"
}
</script>

<style scoped>

  #main-banner {
    background-image: url("/public/img/burger.jpg");
    background-position: 0 auto;
    background-size: cover;
    background-position-y: center;
    height: 200px;
    display: flex;
    align-items: center;
    justify-content: flex-start;
  }

  #main-banner h2 {
    color: #b4b4b4;
    padding-left: 15px;
  }

  @media(min-width:770px) {
    #main-banner {
      background-position: 0 -250px;
      background-size: cover;
      background-position-y: center;
      height: 600px;
      display: flex;
      align-items: center;
      justify-content: flex-start;
    }

    #main-banner h2 {
        color:#fff;
        text-align: center;
        font-size: 60px;
        background-color: #222;
    }
  }

</style>
