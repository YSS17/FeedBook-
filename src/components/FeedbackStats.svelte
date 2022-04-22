<script>
  export let count;
  export let averagerounded;

</script>

<div class="feedback-stats">
  <h4>{count} reviews</h4>
  <h4>Ratings Average: {averagerounded}</h4>
</div>

<style>
  .feedback-stats{
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
</style>