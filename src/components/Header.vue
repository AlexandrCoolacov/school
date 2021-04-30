<template>
 <div class="header">
   <HeaderLogo/>
   <HeaderMenu/>
   <HeaderNav/>
 </div>
</template>

<script>

import HeaderLogo from './HeaderLogo'
import HeaderMenu from './HeaderMenu'
import HeaderNav from './HeaderNav'

export default {
  
  name: 'Header',
  /* props: {
    msg: String
  },  */
  components: {
    HeaderLogo,
    HeaderMenu,
    HeaderNav,
  }
}
</script>

<!-- Add "scoped" attribustyte to limit CSS to this component only -->

<style scoped>
.header {
  margin: 0 auto;
  max-width: 960px;
  min-height: 73px;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr ;
  grid-template-rows: 73px;
  grid-template-areas: 'logo menu nav';
  border-bottom: 2px solid #CCCCCC;
  align-items: center;
  justify-content: center;
  vertical-align: middle;
  text-align: center;
  grid-gap: 15px;
  
  
}

@media (max-width:950px) {
  .header{
    grid-template-columns: 150px 1fr;
    grid-template-rows: 100px 200px;
    grid-template-areas: 
    'menu logo'
    'nav nav';
  } 
}

@media (max-width:475px) {
  .header{
    grid-template-columns: 1fr;
    grid-template-rows: 64px 100px 200px;
    grid-template-areas: 
    'logo logo'
    'menu menu'
    'nav nav';
  } 
}
</style>