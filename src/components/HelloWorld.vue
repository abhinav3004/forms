<template>
  <div class="hello">
  <form>
  <!-- text -->
  <p>
   <label>First Name</label> 
    <input type="text" v-model="msg">
    {{fname}}
  </p>
   <p>
   <label>Last Name</label> 
    <input type="text" v-model="msg">
    {{lname}}
  </p>
  <p>
   <label>User Name</label> 
    <input type="text" v-model="msg">
    {{user}}
  </p>
  <!-- checkbox -->
  <p>
    <input type="checkbox" v-model="checked">
    {{checked ? "yes" : "no"}}
  </p>
  <!-- radio buttons -->
  <p>
    <input type="radio" name="picked" value="one" v-model="picked">
    <input type="radio" name="picked" value="two" v-model="picked">
    {{picked}}
  </p>
  <!-- select -->
  <p>
    <select v-model="selected">
      <option>one</option>
      <option>two</option>
    </select>
    {{selected}}
  </p>
  <!-- multiple select -->
  <p>
    <select v-model="multiSelect" multiple>
      <option>one</option>
      <option>two</option>
      <option>three</option>
    </select>
    {{multiSelect}}
  </p>
  
</form>



  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
    fname      : 'First Name',
    lname      : 'Last Name',
    user       : 'User Name',
    checked  : true,
    picked   : 'one',
    selected : 'two',
    multiSelect: ['one', 'two','three']

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
