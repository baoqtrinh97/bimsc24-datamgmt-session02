<!-- the script is where the js code goes -->
<script setup>
import { ref } from "vue" // you need this to use ref()


let count = ref(0);
function increment() {
  count.value++;
}

let text = ref("");
let inputText = ref("");

function addText() {
  text.value = inputText.value;
}

</script>



<!-- the template is where the html code goes -->
<template>

    <div id="navbar" class="container">  
        <div id="title">Bao's bootcamp website website</div>
        
        <div id="logo">
            <img src="./cow.jpg" alt="macad cow">
    

        </div>
        

    </div>

    <div id="flex">

        <div id="sidebar" class="container"> Sidebar 
          <Button @click="increment">
            <p>You clicked {{ count }} times</p>
          </Button>
        </div>

        <div id="main" class="container"> Text input 
          <input v-model="inputText"/>
          <button @click="addText">
            <p>You typed: {{ text }}</p>
          </button>


        </div>
    </div>

</template>



<!-- style is where the css code goes -->
<style scoped>
#navbar{
  background-color: #ff6fd1;
}

html{
    
    background-color: rgb(59, 59, 59); 
    color: white;
}

body{

    margin:0;
}

div{

    /* put the borders in the inside of container */
    box-sizing: border-box;
}

img{

    height: 100%;
    width: auto;

}

#navbar{

    height: 50px;
    border-color: red;


}

#flex{
    
    display: flex;
    height: calc(100vh - 50px);
}

#sidebar{
    
    width:30%;
    border-color: blue;

}

#main{
    width:70%;
    border-color: green;

}

#title{
    width: 70%;
    float:left;
}

#logo{
    width: 30%;
    height: 100%;
    float:right;
    text-align: right;

}

.container{

    border-style: dotted;
    border-width: 1px;

}

</style>