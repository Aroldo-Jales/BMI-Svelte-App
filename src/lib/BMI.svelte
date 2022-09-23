<script>
  let height;
  let weight;
  let bmi = '...';

  const submitBMIHandler = () => {
    bmi = (weight)/(height*height)
  }
</script>

<form on:submit|preventDefault={submitBMIHandler}>
  <div class="heightInput">
    <input bind:value={height} type="number" placeholder="Height" required>
  </div>
  <div class="weightInput">
    <input bind:value={weight} type="number" placeholder="Weight" required>
  </div>
	<button>Calculate</button>
</form>

<h2 class="bmiResult">
  Your bmi is {bmi}
</h2>
