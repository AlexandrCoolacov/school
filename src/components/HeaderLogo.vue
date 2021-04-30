<template>
<div class="headerLogo">
    <a  href="/">
        <img src="../assets/cloud.svg" alt="">
    </a>
</div>
    
</template>


<script>
export default {
    name: 'HeaderLogo',
}
</script>

<style lang="scss" scoped>
.headerLogo {
    grid-area: logo;
    
    
    /* width: 282px; */
    height: 64px;
    /* text-align: center; */
    /* align-items: center; */
}

@media (max-width:950px) {
  .headerLogo{
    max-width: 100%;
    img{
        position: relative;
        left:-100px;
    }
  } 
}

@media (max-width:700px) {
  .headerLogo{
    max-width: 100%;
    img{
        position: relative;
        float: right;
        
        left: 0;
    }
  } 
}

@media (max-width:700px) {
  .headerLogo{
    max-width: 100%;
    img{
        position: relative;
        float: right;
        
        left: 0;
    }
  } 
}


@media (max-width:475px) {
  .headerLogo{
    max-width: 100%;
    text-align: center;
    align-items: center;
    justify-content: center;
    img{
        position: relative;
        text-align: center;
        align-items: center;
        justify-content: center;
    }
  } 
}

  
  
</style>