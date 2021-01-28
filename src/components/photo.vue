<template>
  <div id="photo"></div>
</template>

<script>
  export default {
    name: 'photo',
  }
</script>

<style>
#photo {
  max-width: 430px;
  height: 457px;
  padding: 40px;
  overflow: hidden;
  background: 0% 100% / cover no-repeat url('../assets/myPhoto.jpg') #E1E0E5;
  background-clip: content-box;
}
</style>