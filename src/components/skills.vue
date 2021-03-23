<template>
  <div id="skills">
    <div class="name_blocks-right">{{ info.skills.name }}</div>
    <div class="content_blocks-right">
      <ul>
        <li v-for="(skill, index) in info.skills.content" :key="index">
          <div>{{ skill.name }}</div>
          <div :class="skill.style" class="skill"></div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "skills",
  props: ["info"],
};
</script>

<style>
#skills {
  margin-top: 10px;
}

#skills ul {
  display: grid;
  grid-template-columns: auto auto;
}

#skills li {
  display: grid;
  grid-template-columns: auto auto;
  justify-content: space-between;
  margin-bottom: 5px;
}

#skills li > div:first-child {
  font-size: 1em;
  text-transform: uppercase;
}

.skill {
  height: 10px;
  width: 140px;
  border-radius: 10px;
  margin-bottom: 10px;
  box-shadow: 1px 1px 1px inset #000;
  margin-right: 50px;
  margin-top: 12px;
}

.skill_20 {
  background: linear-gradient(90deg, #fd5b5f 20%, rgb(255, 255, 255) 20%);
}

.skill_40 {
  background: linear-gradient(90deg, #ffa45b 40%, rgb(255, 255, 255) 20%);
}

.skill_60 {
  background: linear-gradient(90deg, #fd5b5f 60%, rgb(255, 255, 255) 20%);
}

.skill_80 {
  background: linear-gradient(90deg, #fd5b5f 80%, rgb(255, 255, 255) 20%);
}

.skill_100 {
  background: linear-gradient(90deg, #fd5b5f 100%, rgb(255, 255, 255) 20%);
}
</style>

<style>
  @media all and (min-width: 1024px) and (max-width: 1279px) {
    .skill {
      width: 100px;
      margin-top: 7px;
    }
  }
</style>

<style>
  @media all and (min-width: 768px) and (max-width: 1023px) {
    .skill {
      width: 100px;
      margin-top: 9px;
    }
  }
</style>

<style>
  @media all and (min-width: 320px) and (max-width: 767px) {
    .skill {
      width: 10px;
      margin-top: 3px;
    }
  }
</style>

<style>
  @media all and (min-width: 0px) and (max-width: 767px) {
    .skill {
      width: 100px;
      margin-top: 4px;
      margin-right: 0px;
    }

    #skills ul {
      display: grid;
      grid-template-columns: auto;
    }
  }
</style>
