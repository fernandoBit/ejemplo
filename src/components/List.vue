<template>
    <div class="bg-indigo-500 rounded p-3">
        <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
        <label for="jack">Jack</label>
        <input type="checkbox" id="john" value="John" v-model="checkedNames">
        <label for="john">John</label>
        <input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
        <label for="mike">Mike</label>
        <br>
        <span>Checked names: {{ checkedNames }}</span><br>

        <select v-model="selected" id="letras">
            <option v-for="(option,id) in options" :key="id">{{ option.text}}</option>
        </select>
        <span>Selected: {{ selected }}</span>
    </div>
</template>

<script>
export default {
    data(){
        return {
            checkedNames: [], 
            selected: [],
            options: [
                { text: "A", value: "1"},
                { text: "B", value: "2"},
                { text: "C", value: "3"}
            ]
        }
    }
}
</script>

