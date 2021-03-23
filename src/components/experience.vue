<template>
  <div id="experience">
    <div class="name_blocks-right">{{info.experience.name}}</div>
    <div class="content_blocks-right">
      <ul>
        <li v-for="(experience, index) in info.experience.content" :key="index">
          <div class="itemName">{{experience.name}}</div>
          <div class="itemDate">{{experience.date}}</div>
          <div class="itemDescription">{{experience.description}}</div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    props: ['info'],
    name: 'experience',
  }
</script>

<style>

</style>