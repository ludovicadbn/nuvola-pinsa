<template>
  <div class="container">
    <header>
      <div class="slider">
        <div class="topnav">
          <div class="text-center" id="div-logo">
            <img id="logo" src="../assets/img/logo.png" alt="logo nuvola pinsa">
          </div>
          <!-- Navigation links (hidden by default) -->
          <div id="nav-links">
            <ul class="mt-4">
              <li v-for="elm in nav" :key="elm.id">
                <a class="text-capitalize" :href="elm.url">{{elm.name}}</a>
                <hr>
              </li>
            </ul>
          </div>
          <!-- "Hamburger menu" / "Bar icon" to toggle the navigation links -->
          <a href="javascript:void(0);" class="icon" @click="myFunction()">
            <i class="fa fa-bars"></i>
          </a>
        </div>

      </div>
    </header>
    <main>
      <div class="d-xl-flex flex-wrap">
        <div class="w-70 my-2">
          <div class="text-center w-90" id="bakery">
            <img class="mt-4" src="../assets/img/bakery.png">
            <h2 class="fs-20 my-2 text-similblack text-center">A Cloud Of Tastiness</h2>
          </div>
          <div class="text-justify text-lightgray">
            <p class="fs-13">Nuvola comes from Corrado Di Marco’s intuition and his continuous research on flour and leavening methods. With this ready-to-top base, you will taste an incredibly light and digestible product that everyone will love, even those who lead a vegan lifestyle.</p>
          </div>
        </div>
        <div class="mt-4 d-xl-flex">
          <div  class="col-xl-6 d-xl-flex ai-center jc-center">
            <div class="mb-4">
              <div class="w-xl-80">
                <div class="w-80 mt-4">
                  <h2 class="fs-20 my-2 text-similblack">Nuvola classic <br>The original roman pinsa</h2>
                  <p class="text-justify text-lightgray fs-13">A secret mix of flours and long rising time to guarantee digestibility, lightness, and crispness: this is Roman Pinsa, and thanks to Nuvola you can easily prepare it at home. Nuvola is hand-stretched and packed in a modified atmosphere to maintain all the characteristics of a freshly baked pinsa.</p>
                </div>
              </div>
            </div>
          </div>
          <div class="pinsa1 col-xl-6 d-none d-xl-unset">
          </div>
        </div>
      </div>
      <div class="d-xl-flex">
        <div class="pinsa2 col-xl-6 d-none d-xl-unset" id="romana">
        </div>
        <div class="w-80 col-xl-6 d-xl-flex ai-center jc-center">
          <div class="w-xl-80">
            <h2 class="fs-20 my-2 text-similblack">Nuvola multigrain <br>Rustic flavor and lightness</h2>
            <p class="text-justify text-lightgray fs-12">We added whole rye flour, sunflower seeds, pumpkin seeds, flax seeds, oat flour, barley malt and flour to our classic Roman Pinsa, for a more digestible, tasteful, and healthy dough. You will only need to bake it for five minutes with your favourite toppings.</p>
          </div>
        </div>
      </div>
      <div class="d-xl-flex">
        <div class="w-80 col-xl-6 d-xl-flex ai-center jc-center">
          <div class="w-xl-80">
            <h2 class="fs-20 my-2 text-similblack">Nuvola ambient <br>Fragrance at hand, now at room temperature</h2>
            <p class="text-justify text-lightgray fs-12">All the lightness, freshness, taste, and versatility of classic Nuvola, now “out of the fridge”. Nuvola Ambient can be kept at room temperature, coming in handy while doing shopping as well as for at home conservation, without giving up to the famous characteristics of the original Roman Pinsa.</p>
          </div>
        </div>
        <div class="pinsa3 mt-4 col-xl-6 d-none d-xl-unset">
        </div>
      </div>
      <div class="d-xl-flex">
        <div class="impasto col-xl-6 d-none d-xl-unset">
        </div>
        <div class="w-80 col-xl-6 d-xl-flex ai-center jc-center">
          <div class="w-xl-80">
            <h2 class="fs-20 my-2 text-similblack">Crunchy on the outside, fluffy on the inside</h2>
            <p class="text-justify text-lightgray fs-13">Nuvola dough is made with wheat flour, water, sourdough, soy flour, extravirgin olive oil, salt, and yeast, with no added preservatives; it is then left to rise for 72 hours to get a base that is crunchy on the outside and fluffy on the inside, with a characteristic bread-like fragrance and half the calories of a normal pizza base. Incredibly soft and with its unique oval shape, Nuvola Pinsa is perfect for every occasion.</p>
          </div>
        </div>
      </div>
      <div class="d-xl-flex">
        <div class="w-80 mb-4 col-xl-6 d-xl-flex ai-center jc-center">
          <div class="w-xl-80">
            <h2 class="fs-20 my-2 text-similblack">Customise your Nuvola Pinsa!</h2>
            <p class="text-justify text-lightgray fs-12">Preparing your Nuvola Pinsa has never been easier, you just need to put it in the oven for five minutes at maximum temperature. Cooking time can vary depending on the oven type and desired crispness: for a crispier crust, just bake it for one more minute! Based on the ingredients of your choice, toppings can be added before or after cooking the base. Nuvola is available in single or double packs and must be kept in the fridge between 0°C and 4°C. It should only be opened few minutes before use.</p>
          </div>
        </div>
        <div class="pinsa4 col-xl-6">
        </div>
      </div>
      <!-- GALLERY -->
      <div class="text-center w-90 my-2" id="gallery">
        <img class="mt-4 mb-2" src="../assets/img/icon-gallery.png">
        <h2 class="fs-20 text-similblack text-center">Gallery</h2>
      </div>
      <div class="d-flex flex-wrap">
        <div v-for="elm in gallery" :key="elm.id" class="gallery col-4 col-xl-4">
          <img :src="elm.img">
        </div>
      </div>
      <!-- VIDEO -->
      <div class="video d-flex jc-center ai-center" id="video">
        <div class="text-center w-90 my-2">
          <img class="mt-4 mb-2" src="../assets/img/icon-video.png">
          <h2 class="fs-20 text-similblack text-center">Video</h2>
          <span>Watch the Nuvola Pinsa videos! Great tips for topping Nuvola and much more...</span>
          <div class="btn-youtube">
            <span class="text-uppercase"><a href="https://www.youtube.com/channel/UCbGEAjUpX5tjoIfcfhIBg3Q" target="_blank">discover our youtube channel</a></span>
          </div>
        </div>
      </div>
      <!-- ACQUISTA -->
      <div class="acquista d-flex jc-center ai-center" id="acquista">
        <div class="text-center w-90 my-2">
          <img class="mt-4 mb-2" src="../assets/img/logo-white.png">
          <h2 class="fs-20 text-similblack text-center">Where to buy</h2>
          <span>Coming soon...</span>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
export default {
name: 'MainComp',
components : {
},
data(){
  return{
    nav : [
      {
        name : 'home',
        url : '#'
      },
      {
        name : 'a cloud of tastiness',
        url : '#bakery'
      },
      {
        name : "to whet your appetite",
        url : '#romana'
      },
      {
        name : 'gallery',
        url : '#gallery'
      },
      {
        name : 'video',
        url : '#video'
      },
      {
        name : 'where to buy',
        url : '#acquista'
      },
    ],
    gallery : [
      {
        img : require('../assets/img/gallery-1.jpg')
      },
      {
        img : require('../assets/img/gallery-2.jpg')
      },
      {
        img : require('../assets/img/gallery-3.jpg')
      },
      {
        img : require('../assets/img/gallery-4.jpg')
      },
      {
        img : require('../assets/img/gallery-5.jpg')
      },
      {
        img : require('../assets/img/gallery-6.jpg')
      },
      {
        img : require('../assets/img/gallery-7.jpg')
      },
      {
        img : require('../assets/img/gallery-8.jpg')
      },
      {
        img : require('../assets/img/gallery-9.jpg')
      },
    ]
  }
},
methods : {
  myFunction() {
    var x = document.getElementById("nav-links");
    if (x.style.display === "block") {
      x.style.display = "none";
    } else {
      x.style.display = "block";
    }
  } 
}
}
</script>

<style scoped lang='scss'>
.container{
  header{
    padding: 2em 0;
    .topnav {
      overflow: hidden;
      position: relative;
      background-color: transparent;
      #logo{max-width: 100%; height: auto; width: 10%; }
      .fa-bars{cursor: pointer; font-size: 1.3rem; color: #000;}
      #nav-links{
        display: none;
        a{
          color: #fff;
          padding: 0.6em 0em;
          text-decoration: none;
          display: block;
          width: 65%;
          margin: 0 auto;
          font-size: 0.9rem;
          font-weight: 700;
        }
        hr{color: lightgray; width: 70%; margin: 0 auto; }
      }
      a.icon{
        display: block;
        position: absolute;
        left: 30px;
        top: 12px;
      }
    }
  }
  main{
    text-align: center;
    h2{font-size: 1.8rem;}
    #bakery{width: 80%; margin: 0 auto;}
    .pinsa1{
      background-image: url('../assets/img/pinsa_rossa.jpeg');
      background-position: center;
      background-repeat: no-repeat;
      background-size: auto;
      height: 80vh;
    }
    .pinsa2{
      background-image: url('../assets/img/pinsa_verde.jpeg');
      background-position: center;
      background-repeat: no-repeat;
      background-size: auto;
      height: 80vh;
    }
    .pinsa3{
      background-image: url('../assets/img/pinsa_gialla.jpeg');
      background-position: center;
      background-repeat: no-repeat;
      background-size: auto;
      height: 80vh;
    }
    .impasto{
      background-image: url('https://www.nuvolapinsa.com/wp-content/uploads/2021/10/img-01.jpg');
      background-position: left;
      background-repeat: no-repeat;
      background-size: auto;
      height: 80vh;
    }
    .pinsa4{
      background-image: url('https://www.nuvolapinsa.com/wp-content/uploads/2021/10/img-02.jpg');
      background-position: left;
      background-repeat: no-repeat;
      background-size: auto;
      height: 80vh;
    }
    .gallery{
      max-width: 100%;
      height: calc(100vw / 3);
      display: flex;
    }
    .video{
        background-image: url('../assets/img/banner-video.jpg');
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        height: 55vh;
        width: 100%;
        margin: 1em 0;
        h2{
          color: #fff;
          margin-bottom: 0.7em;
          font-size: 2.2rem;
        }
        span{
          color: #fff;
          font-size: 1.2rem;
        }
        .btn-youtube{
          background-color: #b6191d;
          width: 55%;
          margin: 1em auto;
          padding: 1em 0em;
          a{
            color: #fff;
            font-size: 0.9rem;
            font-weight: 700;
            text-decoration: none;
          }
        }
    }
    .acquista{
      background-image: url('../assets/img/banner-acquisto.jpg');
      background-position: center;
      background-repeat: no-repeat;
      background-size: cover;
      height: 55vh;
      width: 100%;
      h2{
        color: #fff;
        margin-bottom: 0.7em;
        font-size: 2.2rem;
      }
      span{
        color: #fff;
        font-size: 1.2rem;
      }
    }
  }
}

// lg
@media screen and (min-width: 1050px) {
  .container{
    header{
      padding: 0em 0em;
      .topnav {
        padding: 1em 1em;
        display: flex;
        justify-content: space-between;
        align-items: center;
        #div-logo{
          margin-left: 1em;
          #logo{width: 100%;}
        }
        .fa-bars{display: none;}
        #nav-links{
          display: unset;
          ul{
            display: flex;
            margin-top: 0;
            padding-left: 2em;
            li{padding: 0 1em;}
          }
          a{
            padding: 0em 0em;
            width: unset;
            margin: 0 auto;
            font-size: 1rem;
          }
          hr{display: none;}
        }
      }
      .slider{
        background-image: url('../assets/img/banner-eng-giust.jpeg');
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        height: 120vh;
        width: 100%;
      }
    }
    main{
      text-align: unset;
      h2{font-size: 2rem;}
      .pinsa1{background-size: cover;}
      .pinsa2{background-size: cover;}
      .pinsa3{background-size: cover;}
      .impasto{background-size: cover;}
      .pinsa4{background-size: cover;}
      .gallery{
        img{max-width: 100%; height: auto; padding: 0.5em;}
      }
      .video{
        .btn-youtube{width: 22%;}
      }
    }
  }
}


@media screen and (min-width: 1300px){
  .container{
    header{
      .slider{
        background-image: url('../assets/img/banner-eng-giust.jpeg');
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        height: 110vh;
        width: 100%;
      }
    }
    main{
      .pinsa1{width: 95%; margin: 0 auto;}
      .pinsa2{width: 95%; margin: 0 auto;}
      .pinsa3{width: 95%; margin: 0 auto;}
      .impasto{width: 95%; margin: 0 auto;}
      .pinsa4{width: 95%; margin: 0 auto;}
    }
  }
  
}

</style>