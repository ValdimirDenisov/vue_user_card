<template>
  <div id="app" class="user-card">
        <MainImg v-bind:img="mainImg"/>
        <UserNick v-bind:nick="nick"/>
        <UserName v-bind:name="name"/>
        <hr>
        <UserLocation v-bind:location="locationU"/>
        <UserMail v-bind:mail="mail"/>
        <UserPhone v-bind:number="phone"/>
    </div>
</template>

<script>
import UserNick from './components/UserNick.vue'
import UserName from './components/UserName.vue'
import UserLocation from './components/UserLocation.vue'
import UserMail from './components/UserMail.vue'
import UserPhone from './components/UserPhone.vue'
import MainImg from './components/mainImg.vue'

export default {
  name: 'App',
  components: {
    UserNick,
    UserName,
    UserLocation,
    UserMail,
    UserPhone,
    MainImg
  }, 
  data () {
    return {
      phone: '+7-495-266-57-34',
      name: 'Иванов Иван Иванович',
      nick: 'romashka',
      locationU: 'Москва, Юбилейная 50',
      mail: 'coldrabbit48@example.com',
      mainImg: '/img/70.0d02ec28.jpg'
    }
  },
  methods: {
    getUserData() {
      this.axios.get('http://37.77.104.246/users/getrandom.php')
        .then((response) => {
          let arr = response['data'];
          this.phone = arr['cellPhone'];
          this.name = arr['firstName'] + " " + arr['lastName'];
          this.nick = arr['gender'];
          this.locationU = arr['country'] + ', ' + arr['city'] + ', ' + arr['street'] + ', ' + arr['houseNumber'];
          this.mail = arr['email'];
          this.mainImg = arr['img'];
        });
    }
  },
  mounted() {
    this.getUserData()
  }
}
</script>

<style>
  .user-card {
      width: 300px;
      padding: 20px;
      border-radius: 10px;
      margin-top: 100px;
      font-family: 'Avenir', Helvetica, Arial, sans-serif;
      color: #2c3e50;
      box-shadow: 0 0 15px 0 rgba(50, 50, 50, 0.2);
      text-align: center;
  }

  .user-card hr {
    height: 4px;
    width: 50px;
    margin: 10px auto;
    background-color: #2c3e50;
  }

</style>
