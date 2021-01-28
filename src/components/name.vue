<template>
  <div id="name">
    <div>Yury</div>
    <div>Chebunin</div>
    <div>Junior Web Developer</div>
  </div>
</template>

<script>
  export default {
    name: 'name',
  }
</script>

<style>
#name {
  background-color: #78A5A3;
  padding: 20px 0px 20px 120px;
  max-width: 392px;
}

#name > div {
  display: inline-block;
}

#name > div:first-child {
  
  color: #e1b16a;
  text-transform: uppercase;
  font-size: 4em;
  line-height: 1.2em;
}

#name > div:nth-child(2) {
  
  color:#ce5757;
  font-weight: 700;
  font-size: 2em;
}

#name > div:last-child {
 
  color:rgba(255, 255, 255, 0.808);
  font-size: 1.7em;
  margin-bottom: 5px;
  text-transform: uppercase;
}
</style>