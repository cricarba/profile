<template>
  <div>
     
      <i class="icon" v-bind:class="contact.icon"></i>
       <a :href="contact.url" target="_blank">
          <span class="SubTitle">{{contact.value}}</span>
        </a>
      
     
  </div>
</template>
<script>
export default {
  name: "Contact",
  props: {
    contact : Object,
  }
};
</script>
<style scoped>
.icon {
  letter-spacing: 0.5em;
  font-size: 1;
 
  line-height: 1.5;
}

@media only screen and (max-width: 600px) {
  .icon {
    font-size: 0.8em;
  }
}
</style>
 

 