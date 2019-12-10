<script>
  import { createEventDispatcher } from 'svelte'
  const dispatch = createEventDispatcher()

  export let type = 'default' // primary, secondary
  export let disabled = false
  export let size = 'default' // small, large
  export let shape = 'round' // circle

  function emitClick(e) {
    dispatch('click', e)
  }
</script>

<button
  class={ `${type} size-${size} shape-${shape}` }
  disabled={ disabled }
  on:click={ emitClick }
>
  <slot />
</button>

<style>
button {
  border: 1px solid;
  box-shadow: 0 2px 0 rgba(0, 0, 0, 0.045);
  border-radius: 4px;
}
.default {
  background-color: #1890ff;
  border-color: #1890ff;
  color: #ffffff;
  height: 32px;
  padding: 0px 15px;
}

/* sizes */
.size-default {
  height: 32px;
  padding: 0px 15px;
  font-size: 14px;
}
.size-small {
  height: 24px;
  padding: 0px 7px;
  font-size: 14px;
}
.size-large {
  height: 40px;
  padding: 0px 15px;
  font-size: 16px;
}

/* shapes */
.shape-circle {
  min-width: 40px;
  border-radius: 50%;
}
</style>
