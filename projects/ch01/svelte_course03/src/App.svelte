<script>
  let name='World';
  let age = 30;

  $: uppercaseName = name.toUpperCase();
  $: console.log(name);
  $: if(name === 'Maximilian') {
    age = 32;
  }
  
  function incrememntAge() {
    age += 1;
  }

  function changeName() {
    name = 'Maximilian';
    console.log('It runs!');
  }
</script>

<h1>Hello {uppercaseName}!</h1>
<h2>My age is {age}</h2>
<button on:click="{incrememntAge}">Change Age</button>
<button on:click="{changeName}">Change Name</button>


<style>
  h1 {
    color: purple;
  }
</style>