<template>
<div>
  <h1 class="noteadd">Add a note</h1>
  <div class="wrapper">
    <div class="cat">Title</div> 
    <div class="search">
      <form class="pure-form">
        <i class="fas"></i><input v-model="titleText" />
      </form>
    </div>
  </div>
  <div class="wrapper">
    <div class="cat">User</div> 
    <div class="search">
      <form class="pure-form">
        <i class="fas"></i><input v-model="userText" />
      </form>
    </div>
  </div>
  <div class="wrapper">
    <div class="cat">Text</div>
    <div class="search">
      <form class="pure-form">
        <i class="fas"></i><input v-model="fieldText" />
      </form>
    </div>
  </div>
  <div class="wrapper">
    <button @click="add()" class="auto">Add Note</button>
  </div>
  
</div>
</template>


<script src="moment.js"></script>
<script>

export default {
  name: 'Home',
  components: {
    
  },
  data() {
    return {
      titleText: '',
      userText: '',
      fieldText: '',
    }
  },
  computed: {
    id() {
      return 100 + this.$root.$data.notes.length + 1;
    },
  },
  methods: {
      add(){
        this.$root.$data.notes = [];
        this.$root.$data.notes = this.$root.$data.new_notes.slice(0);
        var toAdd = {id: this.id, title: this.titleText, date: moment().format("MMM Do YYYY"), user: this.userText, time: moment().format('h:mm:ss a'), text_body: this.fieldText, avatar: 1};
        this.$root.$data.notes.push(toAdd);
        this.$root.$data.new_notes.push(toAdd);
        this.titleText = '';
        this.userText = '';
        this.fieldText = '';
      }
  },
}
</script>

<style scoped>
.cat {
  color:maroon;
  padding-right: 10px;
}
.wrapper{
  padding-bottom: 10px;
}
.noteadd{
  color:maroon;
  text-align:center;
}
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.search {
  border: 1px solid #ccc;
  border-radius: 4px;
  width: 50%;
}

form {
  display: table;
  width: 100%;
}

i {
  display: table-cell;
  padding-left: 10px;
  width: 1px;
}

input {
  display: table-cell;
  font-size: 20px;
  border: none !important;
  box-shadow: none !important;
  width: 100%;
  height: 40px;
}
</style>