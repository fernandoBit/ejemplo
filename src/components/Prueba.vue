<template>
    <div class="bg-teal-900 p-5 flex items-center  ">
        <div id="app-4">
            <ol>
                <li v-for="(todo,id) in todos" class="text-white" :key="id">
                    {{ todo.text }}
                    {{ todo.nombre }}
                </li>
                <li>
                    <button v-on:click="reverseMessage" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">Message</button>
                </li>
                 
            </ol>
             <div v-if="prueba">
                    <list></list>
            </div> 
        </div>
    </div>
</template>

<script>
import list from "@/components/List";
export default {
    data() {
        return {
            prueba: false,
            todos: [
                { text: 'Learn JavaScript', nombre: 'Linea' },
                { text: 'Learn PHP', nombre: 'Hello'}
            ]
        }
    },
    methods:{
        reverseMessage (){
            this.prueba =! this.prueba;
        }
    },
    components: {
        list
    }  
};
</script>