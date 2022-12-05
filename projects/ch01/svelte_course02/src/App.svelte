<script>
  let name='World';
  let age = 30;
  
  function incrememntAge() {
    age += 1;
  }
</script>

<h1>Hello {name}!</h1>
<h2>My age is {age}</h2>
<button on:click="{incrememntAge}">Change Age</button>

<style>
  h1 {
    color: purple;
  }
</style>