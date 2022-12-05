<script>
  import ContactCard from './ContactCard.svelte';

  let name = 'World';
  let title = '';
  let image = '';
  let description = '';
  let age = 30;

  $: uppercaseName = name.toUpperCase();
  $: console.log(name);
  $: if (name === 'Maximilian') {
    age = 32;
  }

  function incrememntAge() {
    age += 1;
  }

  function changeName() {
    name = 'Maximilian';
    console.log('It runs!');
  }

  function nameInput() {
    const enteredValue = event.target.value;
    name = enteredValue;
  }
</script>

<h1>Hello {uppercaseName}!</h1>
<h2>My age is {age}</h2>
<button on:click={incrememntAge}>Change Age</button>
<!-- <button on:click="{changeName}">Change Name</button> -->
<!-- <input type="text" value={name} on:input="{nameInput}" style="border: 10px" /> -->
<input type="text" bind:value={name} />
<input type="text" bind:value={title} />
<input type="text" bind:value={image} />
<textarea rows="3" bind:value={description} />

<ContactCard userName={name} jobTitle={title} {description} userImage={image} />

<style>
  h1 {
    color: purple;
  }
</style>
