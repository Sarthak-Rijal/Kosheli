<template>
  <div class="container">
    <div>
      <div class ="logo">
        <meta name="viewport" content="width=device-width,initial-scale=1.0">    
        <img src="~/assets/logofinal.png" />
        <br/>
        <img src="~/assets/name.png" />
        <br/>

        <div class ="comingSoon">
          <img src="~/assets/comingSoon.png" />
        </div>

      </div>

        <br/>
        
        
        <h5 style = "font-weight: bold">Sign up for emails for the latest news</h5 style = "font-weight: bold">
        <b-form-input id = "email" v-model="text" placeholder="YOUR EMAIL, PLEASE!" pattern="/^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/" required></b-form-input>
        <br/>

        <div>

          <b-button v-on:click="doStuff()" @click="modalShow = !modalShow">Submit</b-button>
          <b-modal v-model="modalShow">Hello From Modal!</b-modal>

        </div>
        <br/>
        
        
      <h5 style = "font-weight: bold">Follow us on our social media for the latest updates.</h5 style = "font-weight: bold">
      <div class="links">
        <a
          href="https://vm.tiktok.com/ZMJGCq61y/"
        >
          <img src="~/assets/tiktok.png" />
        </a>
        <a
          href="https://www.instagram.com/kosheli.co/?hl=en"
        >
          <img src="~/assets/instagram.jpg" />
        </a>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    methods: {
      doStuff () { 
        var email = document.getElementById("email").value;
        if (/^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/.test(email))
        {
          var url = "https://pfh-server.herokuapp.com/api/user/join";
          var method = "POST";
          var postData = JSON.stringify({"email":email});

          var shouldBeAsync = true;

          var request = new XMLHttpRequest();


          request.onload = function () {

            // Because of javascript's fabulous closure concept, the XMLHttpRequest "request"
            // object declared above is available in this function even though this function
            // executes long after the request is sent and long after this function is
            // instantiated. This fact is CRUCIAL to the workings of XHR in ordinary
            // applications.

            // You can get all kinds of information about the HTTP response.
            var status = request.status; // HTTP response status, e.g., 200 for "200 OK"
            var data = request.responseText; // Returned data, e.g., an HTML document.
          }

          request.open(method, url, shouldBeAsync);

          request.setRequestHeader("Content-Type", "application/json;charset=UTF-8");


          // Actually sends the request to the server.
          request.send(postData);
          console.log(postData);

          alert("Thanks you! Stay tuned for the latest news.")


          
        } else {
          alert("You have entered an invalid email address!");
          return (false);
        }
      }
    }
  }
</script>

<style>

.logo {
  top: 5%;
  text-align: center;
  font-family: fantasy ;
}

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}


.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
  justify-content: space-between;
}

.comingSoon img{
  padding-top: 5%;
}


@media only screen 
    and (min-width : 375px)  {

      .comingSoon img{
        height: auto;
        width: 250px;
        padding-top: 5%;
      }
}

@media only screen 
    and (min-width: 375px)  { 

      .comingSoon img{
        height: auto;
        width: 250px;
        padding-top: 5%;
      }
}

@media only screen 
    and (min-width: 375px) { 

      .comingSoon img{
        height: auto;
        width: 250px;
        padding-top: 5%;
      }
}

@media only screen 
    and (min-width: 414px)  { 

      .comingSoon img{
        height: auto;
        width: 250px;
        
      }
}

</style>
