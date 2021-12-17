<template>
  
 
   <div>

    <main class="bg-white max-w-lg mx-auto p-8 my-10 rounded-lg shadow-2xl">
        <section>
            <h3 class="font-bold text-2xl">Welcome </h3>
            <p class="text-gray-600 pt-2 ">Sign in to your account.</p>
        </section>

        <section class="mt-10">
            <form class="flex flex-col">
                <div class="mb-6 pt-3 rounded bg-gray-200">
                    <label class="block text-gray-700  font-bold mb-2 ml-3" for="email">name</label>
                    <input v-model="ngName" type="text" id="email" class="bg-gray-200 rounded w-full text-gray-700 focus:outline-none border-b-4 border-gray-300   px-3 pb-3">
                </div>
                <div class="mb-6 pt-3 rounded bg-gray-200">
                    <label class="block text-gray-700 text-sm font-bold mb-2 ml-3" for="password">password</label>
                    <input  v-model="ngpass" type="password" id="password" class="bg-gray-200 rounded w-full text-gray-700 focus:outline-none border-b-4 border-gray-300  px-3 pb-3">
                </div>
                
                <a v-on:click="move()" class="bg-purple-600 cursor-pointer hover:bg-purple-700 text-white font-bold py-2 rounded shadow-lg hover:shadow-xl transition duration-200" >Sign In</a>
            </form>
        </section>


        <div v-if="error">
            <h1>te equivocaste</h1>
        </div>
    </main>

    
</div>
 
</template>

<script>
export default {


    data(){
        return{
            name:"nico",
            pass:"navarro",
            ngName:"",
            ngpass:"",
            error:false

    }
},

    methods:{

        move(){

            if(this.ngName == this.name && this.ngpass == this.pass){
                console.log(this.name)
                console.log(this.contr)
                this.$router.push('/')

            }else{
                    this.error = true
            }
           
        }

}

}




</script>

<style>

</style>