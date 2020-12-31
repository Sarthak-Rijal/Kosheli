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
        <b><h5 style = "font-weight: bold">Be The First To Know</h5 style = "font-weight: bold"></b>
        <p>Simply register to recieve our newsletters with the latest products and exclusive offers!</p>
        <b-form-input v-model="text" placeholder="YOUR EMAIL, PLEASE!" ></b-form-input>
        <br/>
        <button type="submit" class="btn btn-primary">Submit</button>
        <br/>

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
export default {}
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
        padding-top: 5%;
      }
}

</style>
