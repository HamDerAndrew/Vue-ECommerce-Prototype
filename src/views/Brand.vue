<template>
  <div class="about">
    <intro-header-app :boldHead="spanEl" :heading="heading" :subInfo="subInfo"></intro-header-app>
    <div class="grid-container">
      <div class="hand-design">
        <div class="myimage">
          <img src="../assets/img/handdesign.jpg" alt="tailor items" class="img-responsive">
        </div>
          <div class="mytext">
            <h2>Hand Designed Clothing</h2>
            <h5>established in 2013, avenue fashion Sed dictum elit vel sapien luctus eras</h5>
            <p>Praesent feugiat malesuada tristique maecenas rhoncus diam eget quam vestibulim consectetur, id condimentum leo porttitor. Cum sociis natoque penatibus eta magnis disut parturient montes, nascetur ridiculus mus. Donec sem lorem laoreet tempor un risus vitae, rutrum sodales nibh suspendisse congue metus nunc, id viverra elit loreti rhoncus quis consecteur es. Donec pulvinar tempor lorem a pretium justo interdum.
            </p>
          </div>
      </div>
      <div class="ethical-trading">
        <div>
          <img src="../assets/img/ethical trade.jpg" alt="carrying" class="img-responsive">
        </div>
        <div>
          <h2>Ethical trading</h2>
          <h5>we oversee the working conditions of the people in the supply chain</h5>
          <p>Nullam dapibus consectetur neque, faucibus porttitor purus iaculis sed. Aenean eras dapibus augue, eget dignissim dui maecenas et rhoncus mim, vel semper arcu lorem
  Pellentesque congue justo esteir pellentesque aliquet massa eget posuere tincidunt. Cras viverra ullamcorper nunc accumsan hendrerit. A link </p>
        </div>

      </div>
      <div class="vision">
        <div>
          <video autoplay loop muted class="video-container">
          <source src="../assets/video/advertise-vision-compressed.mp4" type="video/mp4">
            Your browser does not support the video tag.
          </video>
        </div>
        <div>
          <h2>our values, vision and strategy</h2>
          <h5>Avenue Fashion believes in treating employees with care</h5>
          <p>Cras maximus venenatis malesuada. Nulla sagittis elit felis, ac facilisis quam ornare aliquam. Etiam cursus odio vitae dui dignissim, sed tempus lacus tincidunt et donec sapien velit, rhoncus eu nulla a, molestie tempus mi maecenas sagittis ornare.
    Pellentesque sapien mi, tincidunt nec magna vitae, volutpat elementum odioni lorem Aliquam tempor massa vitae augue mattis tempor id in ante ut augue erat, luctus eil.
    </p>
        </div>
      </div>
      <div class="awards">
          <img src="../assets/img/award-2018.png" alt="awards" class="img-responsive">
          <img src="../assets/img/best-award-2017.png" alt="awards" class="img-responsive">
      </div>  
    </div>
  </div>
</template>


<script>
import IntroHeader from '../components/HeaderIntro.vue';

export default {
  data() {
    return {
      spanEl: "The",
      heading: "Brand",
      subInfo: "We are Avenue"
    };
  },
  components: {
    "intro-header-app": IntroHeader
  }
}
</script>

