<template>
  <div class="flex flex-wrap content-center justify-center">

    <div class="flex content-center justify-center container mx-auto mt-6 mb-6">
      <img src="https://placehold.it/400x100" width="200" height="50" class="block" />
    </div>

    <div class="bg-gray-200 shadow-sm w-full sm:w-2/5 md:w-2/5 lg:w-2/5 xl:w-2/5 border-0 sm:border p-0 sm:p-6 rounded block">

      <label class="text-xl text-gray-600 inline-block">What is </label>

      <input type="number" v-model="percentage" class="w-16 m-0 inline-block border py-1 px-3 mt-2 mb-2 text-md font-bold text-gray-600 focus:outline-none hover:border-gray-400 focus:border-gray-500 focus:bg-gray-100" /> <span class="text-xl text-gray-600">&#37; of</span>

      <input type="number" v-model="price" class="w-24 m-0 ml-1 inline-block border py-1 px-3 mt-2 mb-2 text-md font-bold text-gray-600 focus:outline-none hover:border-gray-400 focus:border-gray-500 focus:bg-gray-100 mr-2" />

             <label class="text-xl text-gray-600 inline-block mt-4">Answer:</label>
      <h3 class="inline-block text-2xl font-bold text-gray-800 whitespace-pre-line">{{answer}}&#37;</h3>




<div class="border-gray border border-b-0 border-l-0 border-r-0 block mt-6 mb-6"></div>
   

 


    

      <input type="number" v-model="percentage" class="w-16 m-0 inline-block border py-1 px-3 mt-2 mb-2 text-md font-bold text-gray-600 focus:outline-none hover:border-gray-400 focus:border-gray-500 focus:bg-gray-100" /> <span class="text-sm text-gray-600"> is what percent of </span>

      <input type="number" v-model="price" class="w-24 m-0 ml-1 inline-block border py-1 px-3 mt-2 mb-2 text-md font-bold text-gray-600 focus:outline-none hover:border-gray-400 focus:border-gray-500 focus:bg-gray-100 mr-2" />

             <label class="text-sm text-gray-600 inline-block mt-4">Answer:</label>
      <h3 class="inline-block text-2xl font-bold text-gray-800 whitespace-pre-line">{{answer}}&#37;</h3>
      










       <div class="border-gray border border-b-0 border-l-0 border-r-0 block mt-6 mb-6"></div>
   
 
Want to support this project?<br />All donations are kindly accepted.<br /><br />
<form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top">
<input type="hidden" name="cmd" value="_s-xclick" />
<input type="hidden" name="hosted_button_id" value="B56FZ42KXANV6" />
<input type="image" src="https://www.paypalobjects.com/en_US/GB/i/btn/btn_donateCC_LG.gif" border="0" name="submit" title="PayPal - The safer, easier way to pay online!" alt="Donate with PayPal button" />
<img alt="" border="0" src="https://www.paypal.com/en_GB/i/scr/pixel.gif" width="1" height="1" />
</form>

<strong>BTC:</strong> 3GjNaX7pkB4psrg7oWApLMNEJ7XndsrMNu<br />
<strong>ETH:</strong> 0x81eb7560db09c0F96459eD2327b88F6058056611
      
     

    </div>
<div class="pin-b bottom-o fixed sticky">...</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      price: '1000',
      percentage: '10'
    }
  },
  computed: {
    answer() {  
      // return parseInt(this.price).toFixed(0) * parseInt(this.percentage / 100);
      return ((this.percentage / 100) * this.price).toFixed(2);
    }
  }
}
</script>

<style scoped>
</style>
