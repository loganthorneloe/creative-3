<template>
<div class="wrapper">
  <div class="notes">
    <div class="note" v-for="note in notes" :key="note.id">
    <div class="card">
      <div class="topinfo">
        <h1 class="user">{{note.title}}</h1>
      </div>      
      <div class="container">
        <h4><b>{{note.user}}</b></h4>
        <p>{{note.text_body}}</p>
        <p><i>{{note.date}} {{note.time}}</i></p>
      </div>
    </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'NoteList',
  props: {
    notes: Array,
    new_notes: Array,
  }
}
</script>

<style scoped>
.card {
  /* Add shadows to create the "card" effect */
  box-shadow: 0 4px 8px 0 maroon;
  border-radius: 6px;
  transition: 0.3s;
  width: 100%;
}

/* On mouse-over, add a deeper shadow */
.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

/* Add some padding inside the card container */
.container {
  padding: 2px 16px;
  width: 100%;
}
.user{
  padding-left: 10px;
}
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}
.notes {
  margin-top: 20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
.date{
  text-align: right;
}
.note {
  margin: 10px;
  margin-top: 50px;
  width: 100%;
}
.info {
  background: grey;
  color: maroon;
  padding: 10px 30px;
  height: 80px;
}
.topinfo {
  display: flex;
  text-align: right;
}
.info h1 {
  font-size: 16px;
}
.info h2 {
  font-size: 14px;
}
.info p {
  margin: 0px;
  font-size: 10px;
}
.price {
  display: flex;
}
.moreinfo {
  display:flex;
  background: grey;
}
button {
  height: 50px;
  background: #000;
  color: white;
  border: none;
}
.auto {
  margin-left: auto;
}
</style>