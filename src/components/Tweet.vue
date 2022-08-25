<template>
  <div className="tweet">
    <ProfileImage :image="user.image"/>
    <div className="body">
      <div className="top">
        <User :user="user" />

        <Timestamp :time="timestamp" />
      </div>

      <Message :message="message" />

      <Actions />
        <!-- Font Awesome icons -->
      </div>

    <i class="fas fa-ellipsis-h"></i>
    </div>
</template>
<script>
import ProfileImage from './ProfileImage.vue'
import User from './User.vue'
import Timestamp from './Timestamp.vue'
import Message from './Message.vue'
import Actions from './Actions.vue'

export default {
  name: "Tweet",
  props: {
    user: Object,
    timestamp: String,
    message: String,
    image: String,
  },
  components: {
    ProfileImage,
    User,
    Timestamp,
    Message,
    Actions,
  },
  data() {
    return{

    }
  }
}
</script>


<style scoped>
a {
  color: #42b983;
}
</style>
