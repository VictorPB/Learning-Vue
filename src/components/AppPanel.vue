<template>
  
  <section id="AppPanel">
    <img id="image" :alt="`Imagen del proyecto ${alt}`" :src="image" />
    <p id="title"> {{title}} </p>
    <p id="description"> {{description}} </p>    
  </section>

</template>


<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },
    image: {
      type: String,
      required: true
    },
    alt: {
      type: String
    }
  }
}
</script>


<style>

  #AppPanel {
    background-color: #131416;
    border-radius: 10px;
    align-content: center;
    gap: 30px;
    min-width: 350px;
    max-width: 450px;
    min-height: 300px;
    max-height: 400px;
  }
  
  #title {
    color: #FB6304;
    padding: 10px;
    text-align: center;
    font-size: 25px;
    font-weight: bold;
    margin: 0;
  }

  #description {
    color: #dddddd;
    text-align: justify;
    font-size: 16px;
    padding: 0 30px 30px 30px;
    margin: 0;
  }

  #image {
    border-radius: 10px 10px 0 0;
    width: 100%;
  }
  
</style>