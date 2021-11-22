<template>
  <div>
      <button :class="btnStyle" >{{ buttonText }}</button>
  </div>
</template>

<script>
export default {
    name: 'Button',
    props: ['buttonText', 'btnStyle']
}
</script>

<style>

</style>