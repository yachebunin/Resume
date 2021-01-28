<template>
  <div id="app">
    <section>
      <photo></photo>
      <name></name>
      <profile></profile>
      <contact></contact>
      <reference></reference>
    </section>
    <section>
      <experience :experienceList="experienceList"></experience>
      <skills :skills="skills"></skills>
      <education :education="education"></education>
    </section>
  </div>
</template>

<script>
import photo from "./components/photo.vue";
import name from "./components/name.vue";
import profile from "./components/profile.vue";
import contact from "./components/contact.vue";
import reference from "./components/reference.vue";
import experience from "./components/experience.vue";
import skills from "./components/skills.vue";
import education from "./components/education.vue";

export default {
  name: "app",
  components: {
    photo,
    name,
    profile,
    contact,
    reference,
    experience,
    skills,
    education,
  },
  data() {
    return {
      experienceList: [
        {
          name: "experience number one",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus illo nesciunt odio nisi porro commodi cumque natus, deleniti, voluptate modi quos, iusto cum molestias a repudiandae ipsa esse? Odio, tempora! Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus, sint vel omnis quia officiis numquam similique dolores. Molestias odit voluptatibus libero molestiae ipsum laboriosam. Eius minus nostrum sapiente maiores culpa.",
          date: "2018-2019",
        },
        {
          name: "experience number two",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus illo nesciunt odio nisi porro commodi cumque natus, deleniti, voluptate modi quos, iusto cum molestias a repudiandae ipsa esse? Odio, tempora! Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus, sint vel omnis quia officiis numquam similique dolores. Molestias odit voluptatibus libero molestiae ipsum laboriosam. Eius minus nostrum sapiente maiores culpa.",
          date: "2018-2019",
        },
        {
          name: "experience number three",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus illo nesciunt odio nisi porro commodi cumque natus, deleniti, voluptate modi quos, iusto cum molestias a repudiandae ipsa esse? Odio, tempora! Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus, sint vel omnis quia officiis numquam similique dolores. Molestias odit voluptatibus libero molestiae ipsum laboriosam. Eius minus nostrum sapiente maiores culpa.",
          date: "2018-2019",
        },
      ],
      skills: [
        { name: "js", style: "skill_60" },
        { name: "vue", style: "skill_20" },
        { name: "css", style: "skill_80" },
        { name: "bootstrap", style: "skill_60" },
        { name: "html", style: "skill_80" },
      ],
      education: [
        {
          name: "maou sosh number 9 / ulan-ude, resp. buryatia",
          description:
            "I have finished 11 classes. bla-bla-bla  Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde voluptatum doloremque vel nihil voluptatem ad at saepe architecto culpa expedita aliquam quam ut aut, quidem recusandae, veniam illum ullam repellat?  Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde voluptatum doloremque vel nihil voluptatem ad at saepe architecto culpa expedita aliquam quam ut aut, quidem recusandae, veniam illum ullam repellat?",
          date: "2007-2019",
        },
        {
          name: "maou sosh number 9 / ulan-ude, resp. buryatia",
          description:
            "I have finished 11 classes. bla-bla-bla  Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde voluptatum doloremque vel nihil voluptatem ad at saepe architecto culpa expedita aliquam quam ut aut, quidem recusandae, veniam illum ullam repellat?  Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde voluptatum doloremque vel nihil voluptatem ad at saepe architecto culpa expedita aliquam quam ut aut, quidem recusandae, veniam illum ullam repellat?",
          date: "2007-2019",
        },
      ],
    };
  },
};
</script>

<style>
body {
  background: #444C5C;
}

#app {
  margin: 0px auto;
  font-family: "Crimson Text", serif;
  display: flex;
  flex-wrap: wrap;
  max-width: 1370px;
}

#app > section:first-child {
  border-right: 30px solid #444C5C;
}

.name_blocks-left {
  padding: 5px 0px;
  padding-left: 60px;
  font-size: 2em;
  text-transform: uppercase;
  background: #e1b16a;
}

.content_blocks-left {
  padding: 60px;
  font-size: 1.2em;
  background: #78a5a3;
}

.name_blocks-right {
  position: absolute;
  left: 40px;
  top: 40px;
  background: #444C5C;
  color: #ffffff;
  padding: 5px 220px 5px 40px;
  font-size: 2em;
  text-transform: uppercase;
}

.content_blocks-right {
  padding: 40px;
  padding-top: 120px;
  font-size: 1.2em;
  background: #78a5a3;
}
</style>
