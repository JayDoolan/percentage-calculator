<template>
  <div class="flex flex-wrap content-center justify-center">


      <div v-if="modal" class="bg-gray-800 absolute pin-t pin-l w-full h-screen z-50 flex items-center justify-center">
      <div class="bg-gray-900 rounded w-full sm:w-1/3 ml-6 mr-6">
        <h2 class="float-left text-white font-bold leading-loose pt-2 pl-4 text-sm pb-1"><i class="fa fa-bitcoin text-white"></i> &nbsp; Bitcoin</h2>
        <button v-on:click="modal = !modal" class="float-right border-r-0 border-b-0 border-t-0 w-10 h-10 text-white hover:text-gray-400 text-sm focus:outline-none"><i class="fa fa-times text-xs"></i></button>
        <div class="float-left bg-gray-900 block w-full"></div>
        <div class="float-left p-3 text-white text-sm">

<img src="@/assets/img/btc.png" width="200" height="auto" class="w-1/2 mx-auto mb-4" />

<h3 class="font-bold text-center">3GjNaX7pkB4psrg7oWApLMNEJ7XndsrMNu</h3>



        </div>
      </div>
    </div>




      <div v-if="modal2" class="bg-gray-800 absolute pin-t pin-l w-full h-screen z-50 flex items-center justify-center">
      <div class="bg-gray-900 rounded w-full sm:w-1/3 ml-6 mr-6">
        <h2 class="float-left text-white font-bold leading-loose pt-2 pl-4 text-sm pb-1"><i class="fa fa-paypal text-white"></i> &nbsp; Paypal</h2>
        <button v-on:click="modal2 = !modal2" class="float-right border-r-0 border-b-0 border-t-0 w-10 h-10 text-white hover:text-gray-400 text-sm focus:outline-none"><i class="fa fa-times text-xs"></i></button>
        <div class="float-left bg-gray-900 block w-full"></div>
        <div class="float-left p-3 text-white text-sm">

              <a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=8GLRCJJTZCMSA">
                <img src="https://raw.githubusercontent.com/stefan-niedermann/paypal-donate-button/master/paypal-donate-button.png" alt="Donate with PayPal" />
              </a>
        </div>
      </div>
    </div>








    <div class="flex content-center justify-center container mx-auto mt-6 mb-6">
      <img src="@/assets/img/logo.png" width="200" height="50" class="block" />
    </div>
    

    <div class="bg-gray-200 content-center justify-center shadow-sm w-full sm:w-2/5 md:w-2/5 lg:w-2/5 xl:w-2/5 border-0 sm:border p-8 sm:p-8 rounded block">

    <div class="flex mb-4">
      <div class="w-1/3">

        <label class="text-md text-gray-600 inline-block mr-1">What &nbsp;is</label>

        <input type="number" v-model="percentage" class="w-16 m-0 inline-block border py-1 px-3 mt-2 mb-2 text-md font-bold text-gray-600 focus:outline-none hover:border-gray-400 focus:border-gray-500 focus:bg-gray-100 ml-0 sm:ml-2" /> 

      </div>
      <div class="w-1/3">

        <span class="text-md text-gray-600">&#37;&nbsp; of</span>

        <input type="number" v-model="price" class="w-20 m-0 ml-1 inline-block border py-1 px-3 mt-2 mb-2 text-md font-bold text-gray-600 focus:outline-none hover:border-gray-400 focus:border-gray-500 focus:bg-gray-100 ml-0 sm:ml-2" />

      </div>
      <div class="w-1/3 pl-0 sm:pl-8">

        <label class="text-sm font-bold text-gray-600 block">Answer:</label>
        <h3 class="inline-block text-1xl font-bold text-gray-800 whitespace-pre-line">{{answer}}</h3>

      </div>
    </div>

    <div class="w-full border border-t border-b border-l-0 border-r-0 border-gray-300 mt-4 mb-4"></div>

    <div class="flex mb-4">
      <div class="w-1/3 text-gray-600 text-md">

        <input type="number" v-model="percentage2" class="w-16 m-0 inline-block border py-1 px-3 mt-2 mb-2 text-md font-bold text-gray-600 focus:outline-none hover:border-gray-400 focus:border-gray-500 focus:bg-gray-100" /> &nbsp; is &nbsp; what

      </div>
      <div class="text-gray-600 w-1/3 text-md">

        % &nbsp; of <input type="number" v-model="price2" class="w-20 m-0 ml-1 inline-block border py-1 px-3 mt-2 mb-2 text-md font-bold text-gray-600 focus:outline-none hover:border-gray-400 focus:border-gray-500 focus:bg-gray-100 mr-2" />

      </div>
      <div class="w-1/3 pl-0 sm:pl-8">

        <label class="text-sm font-bold text-gray-600 block">Answer:</label>
        <h3 class="inline-block text-1xl font-bold text-gray-800 whitespace-pre-line">{{answer2}}&nbsp;&#37;</h3>

      </div>
    </div>



 <div class="w-full border border-t border-b border-l-0 border-r-0 border-gray-300 mt-4 mb-4"></div>




 <label class="text-md text-gray-600 block mb-2 mr-2 pb-2">Like Our Site? Support Us</label>

    <button
          v-on:click="modal = !modal" type="button" class="rounded bg-white text-gray-500 hover:text-gray-600 focus:outline-none text-xs h-12 text-center w-12 mr-1" accesskey="">
          <i class="fa fa-bitcoin fa-2x"></i>
    </button>

    <button
          v-on:click="modal2 = !modal2" type="button" class="rounded bg-white text-gray-500 hover:text-gray-600 focus:outline-none text-xs h-12 text-center w-12" accesskey="">
          <i class="fa fa-cc-paypal fa-2x"></i>
    </button>



    </div>


<div class="flex content-center justify-center container mx-auto mt-6 p-8 sm:p-0">
 <div class="bg-white shadow-sm w-full sm:w-2/5 md:w-2/5 lg:w-2/5 xl:w-2/5 border-1 sm:border-0 p-0 sm:p-6 rounded block">
  <h1 class="text-gray-800 font-bold mb-3">Welcome to PercentageOnline.com</h1>
  <p class="text-gray-600 pb-6">Calculate percentages instantly in real time using our percentage calculator. This website was created using mobile first design, so works beautifully across all devices.</p>
</div>
</div>

<p class="text-sm text-gray-500 block mt-6">&copy; 2019 <a href="https://percentageonline.com" target="_blank" class="text-gray-600 font-bold underline">PercentageOnline.com</a>. All rights reserved.</p>


  </div>



  
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      price: '1000',
      price2: '1000',
      percentage: '10',
      percentage2: '10',
      modal: false,
      modal2: false
    }
  },
  computed: {
    answer() {  
      // return parseInt(this.price).toFixed(0) * parseInt(this.percentage / 100);
      return ((this.percentage / 100) * this.price).toFixed(2);
    },
    answer2() {  
      // return parseInt(this.price).toFixed(0) * parseInt(this.percentage / 100);
      return (100 / this.price2 * (this.percentage2)).toFixed(2);
    }
  }
}
</script>

<style scoped>
</style>
