<template>
    <div>
        <h1>Reverse message</h1>
        <p>{{ message }}</p>
        <input type="radio" v-model="message" value="one">
        <input type="radio" v-model="message" value="two">
        <select v-model="message">
                <option disabled="">Choose one</option>
                <option value="one">One</option>
                <option value="two">Two</option>
        </select>
        <button v-on:click="revert">Submit</button>
        <button v-on:click.ctrl="revert">Submit Ctrl</button>
        <button v-on:click.shift="revert">Submit Shift</button>
        <button v-on:click.alt="revert">Submit Alt</button>
        <button v-on:click.meta="revert">Submit Meta</button>
        <button v-on:click.left="revert">Submit Mouse Left</button>
        <button v-on:click.right="revert">Submit Mouse right</button>
        <button v-on:click.middle="revert">Submit Mouse middle</button>

        <p>{{ value }}</p>
        <input type="checkbox" v-model="value">
        <!-- <button v-on:click="revertByComputed">Submit</button> -->
    </div>
</template>
<script>
export default {
 data(){
     return{
     message: 'phuc nguyen',
     value: false
  }
 },

 methods: {
     revert: function() {
         this.message = this.message.split('').reverse().join('');
     }
 },

 computed: {
     revertByComputed: function() {
         this.message = this.message.split('').reverse().join('');
     }
 }
}
</script>
