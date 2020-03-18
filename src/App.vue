<template>
<div id="app">
  <div id="menu">
    <div id="brand">
      <router-link to="/">
        <h1>QuickNotes</h1>
      </router-link>
    </div>
    <div id="side">
      <router-link to="/browse">
        <div class="menu-item browse">
          <h2>Notes</h2>
        </div>
      </router-link>
      <router-link to="/help">
        <div class="menu-item">
          <h2>Help (FAQ)</h2>
        </div>
      </router-link>
    </div>
  </div>
  <router-view />
  <div class="footer">
    <a href="https://github.com/BYU-CS-260-Winter-2020/lab-3b-grocery-store-lathorne">https://github.com/BYU-CS-260-Winter-2020/lab-3b-grocery-store-lathorne</a>
  </div>
</div>
</template>

<style>
* {
  box-sizing: border-box;
}
body {
  margin: 50px 100px;
}
#menu {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-column-gap: 5px;
  grid-template-areas: "brand none side";
  margin-bottom: 10px;
  vertical-align: center;
}
#menu a {
  color: maroon;
  text-decoration: none;
}
#brand {
  grid-area: brand;
  display: flex;
  justify-content: left;
}
#side {
  padding-top: 10px;
  grid-area: side;
  display: flex;
  justify-content: center;
}

.menu-item {
  display: flex;
  flex-direction: column;
}
.menu-item p {
  margin: 0px;
}
.browse {
  margin-right: 50px;
}
.footer {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  background-color: white;
  text-align: center;
  padding: 10px;
}
.footer a{
  color: maroon;
  text-decoration: none;
}
</style>