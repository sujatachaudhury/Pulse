

<template>

<div id="app">
  <div>
<b-navbar toggleable="lg" type="dark" variant="info">
  <b-navbar-brand href="#">SignalMan</b-navbar-brand>

  <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

  <b-collapse id="nav-collapse" is-nav>
    <!--<b-navbar-nav>
      <b-nav-item href="#">Link</b-nav-item>
      <b-nav-item href="#" disabled>Disabled</b-nav-item>
    </b-navbar-nav>-->

    <!-- Right aligned nav items -->
    <b-navbar-nav class="ml-auto">
      <!--<b-nav-form>
        <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
        <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
      </b-nav-form>-->

      <b-nav-item-dropdown text="Rooms" right>
        <b-dropdown-item href="#">Room 1</b-dropdown-item>
        <b-dropdown-item href="#">Room 2</b-dropdown-item>
        <b-dropdown-item href="#">Room 3</b-dropdown-item>
        <b-dropdown-item href="#">Room 4</b-dropdown-item>
      </b-nav-item-dropdown>

      <b-nav-item-dropdown right>
        <!-- Using 'button-content' slot -->
        <template slot="button-content"><em>User</em></template>
        <b-dropdown-item href="#">Profile</b-dropdown-item>
        <b-dropdown-item href="#">Sign Out</b-dropdown-item>
      </b-nav-item-dropdown>
    </b-navbar-nav>
  </b-collapse>
</b-navbar>
</div>

<b-container fluid class="bv-example-row ">
  <b-row>

    <b-col md=4 order="1" order-md="2" class="b" >
      <h3>Log In</h3>
      <div id="connectionModal" class="active info">
        <input type="text" id="usernameInput" placeholder="Enter username" class="inputs"><br>
        <input type="text" id="roomInput" placeholder="Enter room ID" class="inputs"><br>
        <b-button variant="outline-primary" id="connectBtn">Connect</b-button>
    </div>
    <div id="messageControls" class="inactive info">
        <ul id="activeUsers"></ul>
        <ul id="broadcastMessages">
        </ul>
        <textarea id="messageInput" placeholder="Enter message " class="inputs"></textarea><br>
                <b-button variant="outline-primary" id="broadcastBtn">Broadcast</b-button>
        <div id="remoteVideos">
          <!-- REMOTE-VIDEOS -->
        </div>
    </div>
    </b-col>
    <b-col md=8 order="2" order-md="1" class="a" >1 of 3</b-col>
  </b-row>
</b-container fluid>
</div>



</template>

<script>

import HelloWorld from './components/HelloWorld.vue'

export default {
    name: 'app',
    components: {
        HelloWorld
    }
}

</script>
<style>

#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    /*margin-top: 60px;*/
}

.bv-example-row{
  padding-left:0;
  padding-right:0;
}
.a{
  margin-top:30px;
  /*background-color: red;*/
}
.b{
   margin-top:30px;
  /*background-color: blue;*/
}
 .info{
     margin: 10px 0;
 }

 .inputs{
   margin:10px 10px;
 }
</style>
