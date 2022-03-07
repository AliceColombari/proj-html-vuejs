<template>
  <div class="chat">
    <!-- inizio btn open / close chat -->
    <div class="openChatBtn pointer" @click="chatOpen = !chatOpen">
        <!-- chat close -->
        <i class="far fa-comment" v-if="!chatOpen"></i> 
        <!-- chat open / comparsa della x per chiudere chat btn -->
        <!-- <i class="fas fa-times fa-2xs" v-if="chatOpen"></i> -->
    </div>
    <!-- fine btn open / close chat -->


    <!-- inizio box chat -->
    <div class="chatBox" v-if="chatOpen">

      <div class="help">
        <div class="title">How can we help?</div>
        <div class="subtitle">We usually respond in a few hours</div>
      </div>

      <div class="main">
        <label for="name">Name</label>
        <input type="text" id="name">
        
        <label for="subject">Object</label>
        <input type="text" id="subject">
        
        <label for="email">Email address</label>
        <input type="text" id="email">
        
        <label for="how">How can we help?</label>
        <input type="text" id="how">

        <button class="send pointer">Send a message</button>
      </div>

    </div>
    <!-- fine box chat -->

  </div>
</template>

<script>
export default {
  name : 'MyChatBtn',
  data(){
    return{
      chatOpen : false
    }
  }
}
</script>

<style lang="scss">

  .chat {
    position: fixed;
    bottom: 20px;
    right: 50px;
    z-index: 9999;

    .openChatBtn {
      color: white;
      font-size: 2rem;
      font-weight: 700;
      background-color: #527ceb;
      height: 60px;
      width: 60px;
      border-radius: 50%;
      box-shadow: 2px 2px 3px rgba(128, 128, 128, 0.5);
      transition: all 0.3s;
      text-align: center;
      line-height: 60px;

      &:hover{
            background-color: #3063ec;
        }
    }

    .chatBox {
      position: absolute;
      right: 0px;
      bottom: 80px;
      width: 20vw;
      background-color: #fff;
      border-radius: 10px;
      box-shadow: 5px 5px 10px grey;

      .help {
        background-color: #527ceb;
        border-radius: 10px 10px 0 0;
        padding: 20px;
        text-align: center;

        button {
          background-color: unset;
          border: none;
          border-radius: 30px;
          padding: 5px 20px;
          color: white;
        }

        .title {
          color: white;
        }

        .subtitle {
          color: rgba(255, 255, 255, 0.8);
        }
      }

      .main {
        padding: 20px;

        label {
          display: block;
          color: grey;
          margin-bottom: 5px;
        }

        input {
          width: 100%;
          padding: 5px 10px;
          border: 1px solid lightgrey;
          border-radius: 5px;
          margin-bottom: 10px;
        
          &#how{
            padding: 5px 10px 50px;
          }
        }

        .send {
          text-align: center;
          color: white;
          background-color: #527ceb;
          width: 100%;
          border: none;
          border-radius: 5px;
          padding: 15px 0;

          &:hover{
            background-color: #3063ec;
          }
        }
      }
    }
  }
</style>