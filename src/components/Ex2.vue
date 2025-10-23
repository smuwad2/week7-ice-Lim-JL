<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                newitem:'',
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter']
            }
            
        },
        methods:{
            addItem(){
                this.items.push(this.newitem);
                this.newitem = '';
            }
        }


    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
    <ul>
        <li v-for="(item,idx) in items">
            {{ item }}
            <button @click="items.splice(idx,1)">Delete!</button>
        </li>
    </ul>
   <input v-model="newitem" type="text" name="newitem">
   <button @click="addItem">Add!</button>
</template>
