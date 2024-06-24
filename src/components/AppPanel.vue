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


<template>
  
  <section>
    <img :alt="`Imagen del proyecto ${alt}`" :src="image" />
    <h3> {{title}} </h3>
    <p> {{description}} </p>    
  </section>

</template>


<style>

  section {
    background-color: #131416;
    border-radius: 10px;
    margin: 10px;
    align-items: center;
  }
  
  h3 {
    color: #FB6304;
    padding: 10px 10px 10px 10px;
    text-align: center;
  }

  p {
    color: #D6D6D6;
    padding:5px 20px 20px 20px;
    text-align: justify;
  }

  img {
    border-radius: 10px 10px 0 0;
    width: 100%;
  }
  
</style>