<template>
  <div id="photo">
    <div></div>
    <div>{{info.profile.content}}</div>
  </div>
</template>

<script>
  export default {
    name: 'photo',
    props: ['info'],
  }
</script>

<style>

    #photo {
      max-width: 100%;
      height: 450px;
      margin-bottom: 10px;
    }

    #photo > div {
      height: 100%;
      background: center / cover no-repeat url('../assets/myPhoto.jpg');
    }

    #photo > div:last-child {
      display: none;
    }
</style>

<style>
  @media all and (min-width: 768px) and (max-width: 1023px) {
    #photo {
      max-width: 50%;
      height: 350px;
      border-radius: 100%;
      overflow: hidden;
    }

    #photo > div:first-child {
      background: center / cover no-repeat url('../assets/myPhoto.jpg');
    }

    #photo > div:last-child {
      font-size: 30px;
      display: block;
      color: #000;
      position: absolute;
      background: none;
      top: 100px;
      left: 50%;
      height: auto;
    }
  }
</style>


<style>
  @media all and (min-width: 0px) and (max-width: 767px) {
    #photo {
      max-width: 50%;
      height: 150px;
      border-radius: 100%;
      overflow: hidden;
    }

    #photo > div:first-child {
      background: center / cover no-repeat url('../assets/myPhoto.jpg');
    }

    #photo > div:last-child {
      font-size: 15px;
      display: block;
      color: #000;
      position: absolute;
      background: none;
      top: 30px;
      left: 52%;
      height: auto;
    }
  }
</style>
