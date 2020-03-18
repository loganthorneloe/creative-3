<template>
<div>
    <h1 class="noitems">Help</h1>
    <h4 class="question">How does this work?</h4>
    <div class="response">Fill out the form on the home page to add a new note. Select "Notes" in the menu bar to view collection.</div>
    <h4 class="question">Can I browse my notes?</h4>
    <div class="response">On the "Notes" page, enter a note title in the search bar to find the note.</div>
    <h4 class="question">Why do my current notes look like gibberish?</h4>
    <div class="response">When no notes have been recorded, the rest of the notebook is filled with gibberish.</div>
    <h4 class="question">Can I delete my notes?</h4>
    <div class="response">Nope. All notes remain permanently (until you hard reload the page). The search tool will help you find the notes you need if there are too many.</div>
</div>
</template>

<script>
export default {
  name: 'Help',
  components: {
    
  },
  data() {
    return {
      searchText: '',
    }
  },
  computed: {
    items() {
      return this.$root.$data.cart;
    }
  },
}
</script>

<style scoped>
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
.noitems{
  text-align:center;
}
.question{
  padding-bottom: 10px;
}
.response{
  padding-bottom: 10px;
}
</style>