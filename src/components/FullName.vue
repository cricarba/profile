<template>
  <div>
    <br/>
    <span class="letter">{{ FirstName }} {{ LastName }}</span>
    <br/>
    <br/>
    
  </div>
</template>

<script>
export default {
  name: "FullName",
  props: {
    FirstName: String,
    LastName: String
  }
};
</script>

<style scoped>
.letter {
  font-size: 26px;
    line-height: 1.25;
}
 

@media only screen and (max-width: 600px) {
  .letter {
    font-size: 1em;
  }
}
</style>
