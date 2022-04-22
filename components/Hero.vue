<template>
  <div class="Hero container">
    <img src="../assets/svg/cookieMonster.svg" alt="my svg" class="image" />
    <div class="text-container">
      <h1 class="header">Best cookies in Europe</h1>
      <p class="snippet">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Magni, itaque.
        Eligendi culpa saepe rerum quisquam eaque blanditiis animi ducimus
        alias.
      </p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.Hero {
  position: relative;
  display: flex;
  padding: 2rem 0 6rem 0;
  align-items: flex-start;
  justify-content: space-between;
}
.text-container {
  width: 50%;
  margin-top: 4rem;
}
.header {
  font-weight: 900;
  font-size: 5rem;
}
.snippet {
  color: grey;
  font-size: 1.25rem;
}
.image {
  width: 27.5rem;
  margin-top: 2rem;
}
.overlay {
  background: rgba(0, 0, 0, 0);
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
}
.button {
  padding: 1rem 4rem;
  border-radius: 100rem;
  background-color: rgb(231, 81, 43);
  color: white;
  width: 20rem;
  font-weight: 700;
  transition: 0.5s;
}
.button:hover {
  width: 21.5rem;
}
</style>
