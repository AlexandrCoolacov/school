<template>
  <div id="app">
    <Header/>
    <Vitrina/>
    
    
  </div>
</template>

<script>
import Header from './components/Header'
import Vitrina from './components/Vitrina.vue'



export default {
  name: 'App',
  components: {
   Header,
  Vitrina
  },
  mounted() {
     
			 const XHR = ("onload" in new XMLHttpRequest()) ? XMLHttpRequest : XDomainRequest;
        const xhr = new XHR();
        
        xhr.open('POST', 'https://krapipl.imumk.ru:8443/api/mobilev1/update', true);

        xhr.onerror = function() {
            console.log('Ошибка ' + this.status);
        }

        xhr.onload = function() {
            
              const data =JSON.parse(this.responseText);

              console.log(data);
        }

       

        xhr.send();
}
}
</script>

<style>

</style>
