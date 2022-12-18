<script>
  let count = 0;
  let clickPower = 1;
  let upgradeCost = 1;
  const increment = () => {
    count += clickPower;
  }
  const upgradeClickPower = () =>{
    if (count>=upgradeCost){
      clickPower +=1;
      count -= upgradeCost;
      upgradeCost = upgradeCost *2;
    }   
  }
</script>
<main>
<h1>Clicker</h1>
  <div class="ClickerBT">
  <button on:click={increment}>
  Points {count}
</button>
  </div>
 <h1>Buy Upgrade</h1>
 <h3>Current click power : {clickPower}</h3>
 <div class="Upgradecard">
  <button on:click={upgradeClickPower}>
    Upgrade Cost : {upgradeCost}
  </div>
</main>
<style>
</style>
