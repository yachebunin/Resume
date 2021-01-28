<template>
  <div id="experience">
    <div class="name_blocks-right">Experience</div>
    <div class="content_blocks-right">
      <ul>
        <li v-for="(experience, index) in experienceList" :key="index">
          <div class="experienceName">{{experience.name}}</div>
          <div class="experienceDate">{{experience.date}}</div>
          <div class="experienceDescription">{{experience.description}}</div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    props: ['experienceList'],
    name: 'experience',
  }
</script>

<style>
#experience {
   position: relative;
   color: #000;
    max-width: 800px;
}

li {
  display: flex;
  flex-wrap: wrap;
  align-items: flex-end;
  color:rgba(255, 255, 255, 0.808);
}

.experienceName {
  flex-basis: 575px;
  color: #000;
  text-shadow: 2px 2px 7px #fff;
  flex-grow: 1;
  font-size: 1.4em;
  text-transform: capitalize;
  margin-top: 20px;
}	


.experienceName::before {
  content: '\2022';
  margin-right: 5px;
  color: #e1b16a;
  text-shadow: 1px 1px 5px #000;
}

.experienceDate {
  font-size: 1.3em;
  color: #e1b16a;
  text-shadow: 2px 2px 5px #000;
}

.experienceDescription {
    margin-top: 5px;
    color:rgb(233, 233, 233);
}
</style>