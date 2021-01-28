<template>
  <div id="skills">
    <div class="name_blocks-right">Skills</div>
    <div class="content_blocks-right">
      <ul>
        <li v-for="(skill, index) in skills" :key="index">
          <div>{{skill.name}}</div>
          <div :class="skill.style" class="skill"></div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'skills',
    props: ['skills']
  }
</script>

<style>
  #skills {
    border-top: 10px solid #444C5C;
    position: relative;
    color: #000;
      max-width: 800px;
  }

  #skills .content_blocks-right {
    padding: 30px;
    padding-top: 120px;
  }

   #skills > div:first-child {
     color:  #e1b16a;
  }

  #skills ul {
   display: flex;
   flex-wrap: wrap;
   align-items: flex-end;
  }

  #skills li {
    position: relative;
    flex-basis: 50%;
    margin-bottom: 7px;
  }

  #skills li > div:first-child {
    font-size: 1.2em;
    text-transform: uppercase;
    text-shadow: 1px 1px 2px #000;
    margin-left: 10px;
  }

  .skill {
    position: absolute;
    top: 10;
    left: 160px;
    height: 10px;
    width: 150px;
    border-radius: 10px;
    margin-bottom: 10px;
    box-shadow: 1px 1px 2px inset #000;
  }

  .skill_20 {
    background: linear-gradient(90deg, rgb(225, 177, 106) 20%, rgb(255, 255, 255) 20%);
  }

  .skill_40 {
    background: linear-gradient(90deg, rgb(225, 177, 106) 40%, rgb(255, 255, 255) 20%);
  }

  .skill_60 {
    background: linear-gradient(90deg, rgb(225, 177, 106) 60%, rgb(255, 255, 255) 20%);
  }

  .skill_80 {
    background: linear-gradient(90deg, rgb(225, 177, 106) 80%, rgb(255, 255, 255) 20%);
  }

  .skill_100 {
    background: linear-gradient(90deg, rgb(225, 177, 106) 100%, rgb(255, 255, 255) 20%);
  }
</style>