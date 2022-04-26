<template>
  <button v-bind:style="{background, color}">{{value}}</button>
</template>

<script>
export default {
    props: {
        background: {
            type: String
        } ,
        value: {
            type: String
        } ,
        color: {
            type: String
        }
    }
}
</script>
//scoped ensures that the styles are not applied else where
<style scoped>
button {
    background: none;
    color: black;
    border: none;
    border-radius: 5px;
    padding: 10px 40px;
    font-size: 16px;
    cursor: pointer;
}
</style>


