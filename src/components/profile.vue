<template>
  <div id="profile">
    <div class="name_blocks-left">{{info.profile.name}}</div>
    <div class="content_blocks-left">
      {{info.profile.content}}
    </div>
  </div>
</template>

<script>
  export default {
    name: 'profile',
    props: ['info'],
  }
</script>

<style>
  @media all and (min-width: 768px) and (max-width: 1023px) {
    #profile {
      display: none;
      font-size: 20px;
    }
  }
</style>
