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
    ( 
				async () => {
					"use strict";
					

					 function getData() {

					    return new Promise(function (resolve, reject) {
					    	const url = "https://krapipl.imumk.ru:8443/api/mobilev1/update";
					        const xhr = new XMLHttpRequest();

					        xhr.open('POST', url, true);

							

					        xhr.onload = function () {
					            const status = xhr.status;

					            if ( status == 200 ) {
					                resolve(xhr.response);
					            } else {
					                reject(status);
					            }
					        };

							/* xnr.responseType = 'JSON' */

					        xhr.send();
					    });
					}

					const data = await getData();
					console.log(data);
				}
			) ()
}
}
</script>

<style>

</style>
