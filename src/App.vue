<template>
  <div id="app">
    <Header />
    <Content />
  </div>
</template>

<script>
import Header from "@/components/Header";
import Content from "@/components/Content";

export default {
  name: "App",
  data: () => ({}),
  components: {
    Header,
    Content,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Lato&display=swap");

#app {
  color: white;
  font-family: "Lato", sans-serif;
  font-style: normal;
  font-weight: normal;

  margin: 0 auto;
  padding: 0;

  box-sizing: border-box;
}

button {
  border: none;
  background: transparent;
  cursor: pointer;
}

button:active,
button:focus {
  outline: none;
}

input:active,
input:focus {
  outline: none;
}

a {
  text-decoration: none;
  color: #838282;
}
body {
  margin: 0 auto;
}

@media (max-width: 916px) {
  #app {
    min-width: 916px;
  }
}

@media (max-width: 767px) {
  
}
</style>
