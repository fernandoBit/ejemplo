<template>
    <div class="bg-indigo-500 rounded p-3 mt-2">
        <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
        <label for="jack">Jack</label>
        <input type="checkbox" id="john" value="John" v-model="checkedNames">
        <label for="john">John</label>
        <input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
        <label for="mike">Mike</label>
        <br>
        <select v-model="selected">
            <option v-for="(option,id) in options" :key="id" >{{ option.text}}</option>
        </select><br>
        <button class="bg-gray-500 hover:bg-gray-700 text-white font-bold py-2 px-4 rounded" v-on:click="send" > Enviar</button>
    </div>
</template>

<script>
export default {
    data(){
        return {
            checkedNames: [], 
            selected: [],
            options: [
                { text: "A", value: 1},
                { text: "B", value: 2},
                { text: "C", value: 3}
            ],
            count: 0
        }
    },methods:{
        send (){
            for(var i=0; i<this.checkedNames.length; i++) {
                console.log(this.checkedNames[i])
            }
        }
    }
}
</script>

