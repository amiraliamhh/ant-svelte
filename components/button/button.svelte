<script>
  export let type = 'default' // primary, secondary
  export let disabled = false
  export let size = 'default' // small, large
</script>

<button
  class={ `${type} size-${size}` }
  disabled={ disabled }
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
</style>
