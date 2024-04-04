<script>
  let firstName = "Milen";
  let lastName = "Belanger";
  let beltColour = "black";

  $: fullName = `${firstName} ${lastName}`;
  $: console.log(beltColour);

  const handleClick = () => {
    beltColour = "red";
  };
  const handleInput = (event) => {
    beltColour = event.target.value;
  };
</script>

<main>
  <p>Hello, {fullName}! You have {beltColour} belt</p>
  <input type="text" bind:value={beltColour} />
  <input type="text" bind:value={firstName} />
  <input type="text" bind:value={lastName} />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
