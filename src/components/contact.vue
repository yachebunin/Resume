<template>
  <div id="contact">
    <div class="name_blocks-left">{{info.contact.name}}</div>
    <div class="content_blocks-left">
      <ul>
        <li v-for="(item, index) in info.contact.content" :key="index">
          <div :id="item.id"></div>
          <div><a :href="item.href">{{item.content}}</a></div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'contact',
    props: ['info'],
  }
</script>

<style>
#contact {
  margin-top: 10px;
}

#contact ul {
  display: grid;
  padding-left: 0px;
  justify-content: center;
}

#contact li {
  display: grid;
  grid-template-columns: 50px auto;
  justify-content: start;
  margin-bottom: 10px;
}

#contact li > div:first-child {
  height: 50px;
}

#contact li > div:last-child {
  margin-top: 5px;
  margin-left: 30px;
}

#contact li:last-child {
  margin-bottom: 0px;
}

#contact a {
  text-decoration: none;
  color: #fff;
}

#contact a:hover, #contact a:active {
  text-decoration: underline;
}

#phone, #location, #gmail, #social {
  width: 50px;
}

#phone {
  background: no-repeat url('../assets/phone.png');
}

#location {
  background: no-repeat url('../assets/location.png');
}

#gmail {
  background: no-repeat url('../assets/gmail.png');
}

#social {
  background: no-repeat url('../assets/social.png');
}
</style>

<style>
  @media all and (min-width: 1024px) and (max-width: 1279px) {
    #contact li {
      grid-template-columns: 25px auto;
    }

    #contact li > div:first-child {
      height: 25px;
    }

    #contact li > div:last-child {
      margin-top: 0px;
    }

    #phone {
      background: no-repeat url('../assets/phone1024.png');
    }

    #location {
      background: no-repeat url('../assets/location1024.png');
    }

    #gmail {
      background: no-repeat url('../assets/gmail1024.png');
    }

    #social {
      background: no-repeat url('../assets/social1024.png');
    }
  }
</style>

<style>
  @media all and (min-width: 768px) and (max-width: 1023px) {
    #contact li > div:last-child {
      margin-top: 10px;
    }
  }
</style>

<style>
  @media all and (min-width: 0px) and (max-width: 767px) {
    #contact li > div:last-child {
      margin-top: 1px;
    }

    #contact li {
      grid-template-columns: 25px auto;
      margin-bottom: 10px;
    }

    #contact li > div:first-child {
      height: 25px;
    }

   #phone {
      background: no-repeat url('../assets/phone1024.png');
    }

    #location {
      background: no-repeat url('../assets/location1024.png');
    }

    #gmail {
      background: no-repeat url('../assets/gmail1024.png');
    }

    #social {
      background: no-repeat url('../assets/social1024.png');
    }
  }
</style>
