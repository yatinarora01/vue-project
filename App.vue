<template>
<router-view />

</template>

<script>
export default {
  name: 'App',
 
}
</script>

<style>
#app {
  text-align: center;
  color: #2c3e50;
  padding: 20px;
}

.nav-link {
  display: inline-block;
  padding: 10px 20px;
  margin: 0 10px;
  text-decoration: none;
  color: #3498db;
  border: 1px solid #3498db;
  border-radius: 5px;
  transition: background-color 0.3s, color 0.3s;
}

.nav-link:hover {
  background-color: #3498db;
  color: #ffffff;
}

/* Additional global styles for buttons (adjust as needed) */
button {
  cursor: pointer;
  padding: 10px 20px;
  font-size: 16px;
  border: 1px solid #3498db;
  background-color: #3498db;
  color: #ffffff;
  border-radius: 5px;
  transition: background-color 0.3s, color 0.3s;
}

button:hover {
  background-color: #ffffff;
  color: #3498db;
}
</style>
