<template>
  <div id="education">
    <div class="name_blocks-right">education</div>
    <div class="content_blocks-right">
      <ul>
        <li v-for="(educationItem, index) in education" :key="index">
          <div class="educationName">{{educationItem.name}}</div>
          <div class="educationDate">{{educationItem.date}}</div>
          <div class="educationDescription">{{educationItem.description}}</div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'education',
    props: ['education']
  }
</script>

<style>
  #education {
    border-top: 10px solid #444C5C;
    position: relative;
    color: #000;
      max-width: 800px;
}

.educationName {
  flex-basis: 568px;
  color: #000;
  text-shadow: 2px 2px 7px #fff;
  flex-grow: 1;
  font-size: 1.4em;
  text-transform: capitalize;
  margin-top: 20px;
}	


.educationName::before {
  content: '\2022';
  margin-right: 5px;
  color: #e1b16a;
  text-shadow: 1px 1px 5px #000;
}

.educationDate {
  font-size: 1.4em;
  color: #e1b16a;
  text-shadow: 2px 2px 5px #000;
}

.educationDescription {
    margin-top: 5px;
    color:rgb(233, 233, 233);
}
</style>