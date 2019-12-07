<script>
    export let type = 'default'
</script>

<button class={ type } >
    <slot />
</button>

<style>
button {
    border: none;
}
.default {
    background-color: #1890ff;
}
</style>
