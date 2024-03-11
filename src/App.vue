<script setup>
import Product from './components/Product.vue'
import whatsIcon from '../public/svg/icons8-whatsapp.svg'


function smoothScroll(target, duration) {
            var target = document.querySelector(target);
            var targetPosition = target.getBoundingClientRect().top;
            var startPosition = window.pageYOffset;
            var distance = targetPosition - startPosition;
            var startTime = null;

            function animation(currentTime) {
                if (startTime === null) startTime = currentTime;
                var timeElapsed = currentTime - startTime;
                var run = easing(timeElapsed, startPosition, distance, duration);
                window.scrollTo(0, run);
                if (timeElapsed < duration) requestAnimationFrame(animation);
            }

            function easing(t, b, c, d) {
                t /= d / 2;
                if (t < 1) return c / 2 *t * t + b;
                t--;
                return -c / 2 * (t * (t - 2) - 1) + b;
            }

            requestAnimationFrame(animation);
}



</script>



<template>

<div class="body">
  <header>

    <img class="logo" src="./img/BESTSOUNDLOGO.png" alt="Bestsound Logo">
    <!-- <p class="logo">Bestsound</p> -->
    <div class="links">
      <a href="#hero-header" @click="smoothScroll('#hero-header', 200)">Inicio</a>
      <a href="#about" @click="smoothScroll('#about', 1000)">Sobre Nosotros</a>
      <a href="#productos" @click="smoothScroll('#productos', 1000)">Productos</a>
      <a href="#contact" @click="smoothScroll('#contact', 1000)">Contacto</a>
    </div>
  
  </header>


  <main>
  
  <div class="hero-header" id="hero-header">
  
    <div class="textHeader">
      <p>FABRICANDO DESDE 2001</p>

      <h1>TRANSFORMADORES <pre/>
        AUTOTRANSFORMADORES <pre/> 
        FUENTES DE ALIMENTACIÓN  </h1>
    </div>
    <img src="./img/HERO-HEADER-PRODUCTOS.png" alt="Imagen de transformadores autotransformadores fuente de alimentacion y un modulo de rele">  

    
  </div>


  <div class="custom-shape-divider-top-1710030648">
    <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
        <path d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z" class="shape-fill"></path>
    </svg>
  </div>


  <div class="about" id="about">
  
    <div class="about-us">
      <h2>SOBRE NOSOTROS</h2>
      <p>Somos una empresa Argentina con más de 20 años de experiencia en la fabricación de transformadores, autotransformadores y fuentes de alimentación para la industria electrónica, eléctrica y comercios del gremio.
        Brindamos una atención personalizada, desarrollando el producto a medida de las necesidades de cada cliente, priorizando siempre la seguridad, calidad y costo. Asegurando que el producto cumpla con las necesidades del desarrollo del cliente. 
        Fabricamos pequeñas y grandes series y contamos con un amplio abanico de opciones para atender a la industria, comercios, importadores y desarrolladores.        
        </p>
    </div>
  
    <div class="what-we-do">
      <h2>Que hacemos</h2>
      <ul>
        <li>Transformadores con pines para montaje en circuitos impresos</li>
        <li>Transformadores con borneras para instalaciones industriales</li>
        <li>Transformadores con terminales crimpeados según necesidad del cliente</li>
        <li>Fuentes de alimentación lineales y reguladas</li>
        <li>Fuentes de alimentación con salida de corriente alterna</li>
        <li>Cargadores para baterías de gel</li>
        <li>Fuentes de alimentación de corriente alterna con pulsador para apertura de pestillos eléctricos</li>
        <li>Placa relé auxiliar de sirena</li>
        <li>Autotransformadores para equipos con alimentación a 110 Volts</li>
      </ul>
    </div>
  
  </div>

  
  <div class="custom-shape-divider-top-1710031150">
    <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
      <path d="M985.66,92.83C906.67,72,823.78,31,743.84,14.19c-82.26-17.34-168.06-16.33-250.45.39-57.84,11.73-114,31.07-172,41.86A600.21,600.21,0,0,1,0,27.35V120H1200V95.8C1132.19,118.92,1055.71,111.31,985.66,92.83Z" class="shape-fill"></path>
    </svg>
  </div>

  <div class="product-container">
    <div class="productos" id="productos">
    
      <Product class="product" img="TRAFO-CON-PINES.png" alt="Transformador con pines para montaje en PCB" text="Transformadores con pines para montaje en circuitos impresos"/>
      <Product class="product" img="TRAFO-CON-MOLEX.png" alt="Transformador con terminales molex" text="Transformadores con terminales crimpeados"/>
      <Product class="product" img="TRAFO-CON-TERMINALES.png" alt="Transformador con terminales de bornera" text="Transformadores con salida de borneras"/>
      <Product class="product" img="FUENTE-ALIMENTACION.png" alt="Fuente de alimentación CC CA con ficha de alimentación" text="Fuentes de alimentación CC y CA"/>
      <Product class="product" img="CARGADOR-BATERIA.png" alt="Cargador de bateria de gel" text="Cargador de bateria de gel"/>
      <Product class="product" img="MODULO-RELE.png" alt="Modulo de relé" text="Placa relé auxiliar de sirena"/>
      <Product class="product" img="TRAFO-CERRADURA.png" alt="Transformador para apertura de cerradura electrica con pulsador" text="Transformador para apertura de cerradura electrica con pulsador"/>
      <Product class="product" img="AUTO-TRAFO.png" alt="Autotransformador 220/110 de 1500 watts" text="Autotransformadores 220/110 desde 50 a 1500 watts"/>
      
      
      
      </div>
  </div>
  
  </main>


  <div class="custom-shape-divider-top-1710034157">
    <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
        <path d="M985.66,92.83C906.67,72,823.78,31,743.84,14.19c-82.26-17.34-168.06-16.33-250.45.39-57.84,11.73-114,31.07-172,41.86A600.21,600.21,0,0,1,0,27.35V120H1200V95.8C1132.19,118.92,1055.71,111.31,985.66,92.83Z" class="shape-fill"></path>
    </svg>
  </div> 


  <footer class="contact" id="contact">
     

    <div class="phone-contact">
      <whatsIcon class="whatsIcon"/>
      <a href="https://wa.me/+5491167259661">11-6725-9661</a>
    </div>
    <a href="mailto:trafosbestsound@hotmail.com" >Email de contacto</a>
    <p>Chivilcoy 6038 Villa Ballester Buenos Aires Argentina</p>
    
    
  </footer>
</div>


</template>



<style scoped>





.body{
  width: 100vw;
  
}

header{
  display: flex;
  align-items: center;
  /*background-color: rgb(65, 87, 255);*/
  background-color: white;
  width: 100vw;
  justify-content: space-between;
  flex-wrap: wrap;

}




.logo{
  font-size: 40px;
  margin: 0 20px;
  /*font-weight: bold;
  font-style: italic;*/
  object-fit: contain;
  max-width: 577.11px;
  max-height: 70px;
  padding-left: 10px;
  justify-self: flex-start;
  color: black;
}

.links{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-content: center;
  justify-self: flex-end;
  text-wrap: nowrap;

}

.links a{
  color: black;
  text-decoration: none;
  margin: 0px 20px;
  height: 30px;
  padding-top: 3px;
  text-align: center;
  padding-left: 5px;
  padding-right: 5px;
  transition: all 0.2s ease-in;
}

.links a:hover{
  color: #0068ae;
}


.hero-header{
  display: flex;
  /*grid-template-columns: 50% 50%;*/
  flex-wrap: wrap;

  align-items: center;
  justify-content: space-evenly;
  background-color: #0068ae;
  text-wrap: nowrap;
}

.hero-header .textHeader h1{
  font-size: 40px;
}

.hero-header .textHeader{
  padding-top: 20px;
  color: white;
}

.hero-header img{

  max-width: 675px;
  max-height: 675px;

}

.custom-shape-divider-top-1710030648 {
  position: relative;
  /*top: 0;
  left: 0;*/
  background-color: #faf9f9;
  width: 100%;
  overflow: hidden;
  line-height: 0;
}

.custom-shape-divider-top-1710030648 svg {
  position: relative;
  display: block;
  width: calc(121% + 1.3px);
  height: 143px;
  margin-top: -1px;

}

.custom-shape-divider-top-1710030648 .shape-fill {
  fill: #0068AE;
  
}




.about{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  background-color: #faf9f9;
  padding: 50px 0px;
}

.about-us{
  max-width: 600px;
  min-width: 540px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin: 20px;
  background-color: #fafafa;
  padding: 10px;
  border-radius: 20px;
  box-shadow: 0px 0px 10px 0px rgba(0,0,0,0.54);
}

.about-us p{
  margin-top: 5px;
}

.about-us h2{
  font-weight: bold;
  color: #1f6694;
}

.what-we-do{
  max-width: 600px;
  min-width: 540px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin: 20px;
  background-color: #fafafa;
  padding: 10px;
  border-radius: 20px;
  box-shadow: 0px 0px 10px 0px rgba(0,0,0,0.54);
}

.what-we-do p{
  margin-top: 5px;
}

.what-we-do h2{
  font-weight: bold;
  color: #1f6694;
}

.custom-shape-divider-top-1710031150 {
  position: relative;
  /*top: 0;
  left: 0;*/
  width: 100%;
  overflow: hidden;
  line-height: 0;
  transform: rotate(180deg);
  background-color: #3d94ce;
}

.custom-shape-divider-top-1710031150 svg {
  position: relative;
  display: block;
  width: calc(121% + 1.3px);
  height: 143px;
  margin-top: 1px;

}

.custom-shape-divider-top-1710031150 .shape-fill {
  fill: #FAF9F9;
}

.product-container{
  display: flex;
  justify-content: center;
  background-color: #3d94ce;
  padding: 30px 0px;
}

.productos{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  max-width: 1650px;
  text-align: center;
}


.custom-shape-divider-top-1710034157 {
  position: relative;
  /*top: 0;
  left: 0;*/
  width: 100%;
  overflow: hidden;
  line-height: 0;
  transform: rotate(180deg);
}

.custom-shape-divider-top-1710034157 svg {
  position: relative;
  display: block;
  width: calc(100% + 1.3px);
  height: 19px;
  margin-top: 1px;

}

.custom-shape-divider-top-1710034157 .shape-fill {
  fill: #3d94ce;
}


footer{
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 10px 0px;
  
}

footer a{
  color: black;
}

footer .phone-contact{

  display: flex;
  align-items: center;
  font-size: 20px;


}

footer .whatsIcon{
  scale: 90%;
}



@media only screen and (max-width: 1083px) {
  header{
    justify-content: center;
  }

  header .links{
    margin: 10px 0px;
  }

  header .links a{
    margin: 0px 50px;
  }

}

@media only screen and (max-width: 706px){
  header .links a{
  margin: 0px 15px;


  }

}

@media only screen and (max-width: 674px) {

  .hero-header img{
    max-width: calc(675px/2);
    max-height: calc(675px/2);
  }

  .about-us{
    min-width: 300px;
    /*display: flex;
    flex-direction: column;
    justify-content: center;*/
    align-items: center;
    text-align: center;
    /*margin: 20px;
    background-color: #fafafa;
    padding: 10px;
    border-radius: 20px;
    box-shadow: 0px 0px 10px 0px rgba(0,0,0,0.54);*/
  }
  
  
  .what-we-do{
    min-width: 300px;

    align-items: center;
    text-align: center;
  }

  .hero-header .textHeader h1{
    font-size: 30px;
  }
  .hero-header .textHeader p{
    font-size: 12px;
  }
  
  .logo{

    max-width: calc(577.11px/1.5);
    max-height: calc(70px/1.5);

  }  


  .custom-shape-divider-top-1710030648 svg {
    height: 71px;
    
  }


  .custom-shape-divider-top-1710031150 svg {
    height: 71px; 

  }

}

@media only screen and (max-width: 426px){


  header .links a{
    
    margin: 0px 10px;
  
  }

}


@media only screen and (max-width: 418px){

  header .links a{
    margin: 0px 10px;
  }

  .hero-header .textHeader h1{
    font-size: 25px;
  }

  .hero-header .textHeader p{
    font-size: 10px;
  }

  .hero-header img{
    max-width: calc(675px/2.5);
    max-height: calc(675px/2.5);
  }


  .custom-shape-divider-top-1710030648 svg {
    height: 71px;
    
  }


  .custom-shape-divider-top-1710031150 svg {
    height: 71px; 

  }


}

@media only screen and (max-width: 386px){
  header .links a{
    font-size: 12px;
  }

  .logo{

    max-width: calc(577.11px/2);
    max-height: calc(70px/2);

  }  

  .custom-shape-divider-top-1710030648 svg {
    height: 36px;
  }


  .custom-shape-divider-top-1710031150 svg {
    height: 36px;
  }

}



</style>
