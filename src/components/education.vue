<template>
  <div id="education">
    <div class="name_blocks-right">{{info.education.name}}</div>
    <div class="content_blocks-right">
      <ul>
        <li v-for="(education, index) in info.education.content" :key="index">
          <div class="itemName">{{education.name}}</div>
          <div class="itemDate">{{education.date}}</div>
          <div class="itemDescription">{{education.description}}</div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'education',
    props: ['info']
  }
</script>

<style>
  #education {
    margin-top: 10px;
}
</style>