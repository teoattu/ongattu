<script>
  let isOpen = false
</script>
<div class="dropdown__listitem" on:click={()=>{isOpen = !isOpen}}>
  <slot name="icon"></slot>
  <div class="dropdown__title">
    <slot name="title"></slot>
  </div>
  {#if !isOpen}
    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6" />
    </svg>
  {:else}
    <svg xmlns="http://www.w3.org/2000/svg" className="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
      <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M20 12H4" />
    </svg>
  {/if}
</div>
{#if isOpen}
  <div class="dropdown__content">
    <slot name="content"></slot>
  </div>
{/if}
<style>
  .dropdown__listitem {
    width: 100%;
    height: 2rem;
    background-color: #f0f0ff;
    border-radius: 10000px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 1rem;
    margin-top: 2rem;
  }
  .dropdown__content{
    width: 70%;
    margin: 1rem;
  }
  .dropdown__title{
    padding: 0.5rem;
    flex-grow: 3;
    display: flex;
    align-items: center;
  }
</style>