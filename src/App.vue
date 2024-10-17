<script setup>
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import Slider from "./components/Slider.vue";
import Reviews from "./components/Reviews.vue";
import Accordion from "./components/Accordion.vue";
import Footer from "./components/Footer.vue";
import "v-slick-carousel/style.css";
import { VSlickCarousel } from "v-slick-carousel";

const heroData1 = {
  caption: "ALIQUAM CONSECTETUR",
  lemon: "QUISQUE LUCTUS VARIUS MASSA",
  img1: new URL(
    "./assets/images/mobile_images/hero/hero_img--top.png",
    import.meta.url
  ).href,
  img2: new URL(
    "./assets/images/mobile_images/hero/hero_img--bottom.png",
    import.meta.url
  ).href,
};
const bes = "\n";
const caption = `NULLAM PULVINAR${bes}SUSCIPIT EST, VEL VULPUTATE`;
const heroData2 = {
  caption: caption,
  lemon: "SED AT EX EU VELIT FAUCIBUS",
  img1: new URL(
    "./assets/images/mobile_images/hero/hero2_img--top.png",
    import.meta.url
  ).href,
  img2: new URL(
    "./assets/images/mobile_images/hero/hero2_img--bottom.png",
    import.meta.url
  ).href,
};

const heroData3 = {
  caption: "NULLAM PULVINAR SUSCIPIT EST, VEL VULPUTATE",
  lemon: "MAECENAS EX DIAMEGET EGET",
  img1: new URL(
    "./assets/images/mobile_images/hero/hero-money.png",
    import.meta.url
  ).href,
  img2: new URL(
    "./assets/images/mobile_images/hero/hero-bottom.png",
    import.meta.url
  ).href,
  img3: new URL(
    "./assets/images/mobile_images/hero/hero-arrow.png",
    import.meta.url
  ).href,
};

const settings = {
  groupsToShow: 2,
  groupsToScroll: 2,
  arrows: true,
  infinite: true,
  responsive: [
    {
      breakpoint: 600,
      settings: {
        groupsToShow: 1,
        groupsToScroll: 1,
      },
    },
  ],
};

const settings2 = {
  groupsToShow: 1,
  groupsToScroll: 1,
  arrows: true,
  infinite: true,
};
</script>

<template>
  <Header />
  <section class="section-content">
    <div class="comp__hero1">
      <Hero
        :caption="heroData1.caption"
        :lemon="heroData1.lemon"
        :img1="heroData1.img1"
        :img2="heroData1.img2"
        img3=""
      />
    </div>
    <div class="content">
      <h3 class="content__caption caption">Neque porro quisquam: Kalina</h3>
      <p class="content__text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare
        purus non orci suscipit, vitae posuere magna eleifend. Fusce cursus sed
        dui et volutpat. Donec suscipit sodales arcu, eu aliquam lectus
        convallis eget. Sed luctus nec tellus at luctus. Aliquam purus orci,
        cursus sed hendrerit sit amet, tincidunt eget nibh. Proin pulvinar nunc
        id tortor feugiat eleifend. Quisque nec consectetur leo, et blandit
        nisi. Maecenas ac libero eget elit gravida blandit. Vivamus tempor
        imperdiet nisl a vestibulum. Duis gravida sodales nisi nec pellentesque.
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare
        purus non orci suscipit, vitae posuere magna eleifend.
      </p>
      <!-- <div class="youtube">
        <iframe
          width="330"
          height="315"
          src="https://www.youtube.com/embed/bmQwZhcZkbU?si=iMyJMqrWrXr81AMF"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin"
          allowfullscreen
        ></iframe>
      </div> -->
    </div>
    <div class="gallery">
      <img src="./assets/images/desktop_images/gallery/1.png" alt="" />
      <img src="./assets/images/desktop_images/gallery/2.png" alt="" />
      <img src="./assets/images/desktop_images/gallery/3.png" alt="" />
      <img src="./assets/images/desktop_images/gallery/4.png" alt="" />
      <img src="./assets/images/desktop_images/gallery/5.png" alt="" />
      <img src="./assets/images/desktop_images/gallery/6.png" alt="" />
      <img src="./assets/images/desktop_images/gallery/7.png" alt="" />
    </div>
  </section>
  <div class="container">
    <Slider />
  </div>
  <section class="section-aenean">
    <div class="aenean text">
      <h3 class="text__caption">Aenean lacus mi efficitur in venenatis</h3>
      <ul class="text__list">
        <span>Venenatis:</span>
        <li>
          ⦁ Quisque luctus varius massa, in gravida arcu condimentum in. Vivamus
          auctor eleifend metus, ac efficitur metus tempor ullamcorper. Praesent
          sed facilisis sem, eu blandit nisl. Sed fringilla, nisl id consequat
          fringilla, leo magna tempus dolor, euismod tincidunt lectus felis sed
          tellus.
        </li>
        <li>
          ⦁ Mauris aliquam sagittis erat at facilisis. Aliquam erat volutpat.
          Morbi efficitur elementum sem ac laoreet. Ut ut risus in erat iaculis
          porta ac vitae elit. Proin et felis eget risus venenatis lobortis.
          Duis rutrum orci ac placerat rhoncus.
        </li>
        <li>
          ⦁ Quisque nec ligula sodales, mattis mauris sit amet, ullamcorper
          lorem. Integer hendrerit, mi non luctus pulvinar, eros nunc tristique
          mi, nec placerat urna lacus ut justo. Donec vitae sapien sed lorem
          venenatis aliquet.
        </li>
        <li>
          ⦁ Ut cursus imperdiet mi, id pellentesque arcu cursus at. Mauris
          aliquam sagittis erat at facilisis. Aliquam erat volutpat. Morbi
          efficitur elementum sem ac laoreet.
        </li>
        <li>
          ⦁ Aliquam ut lorem augue. Vestibulum quis ullamcorper leo, ac maximus
          est. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices
          posuere cubilia curae.
        </li>
        <li>
          ⦁ Praesent sed facilisis sem, eu blandit nisl. Sed fringilla, nisl id
          consequat fringilla, leo magna tempus dolor, euismod tincidunt lectus
          felis sed tellus.
        </li>
      </ul>
      <div class="carousel carouselAenean">
        <VSlickCarousel v-bind="settings">
          <div class="slide">
            <img
              src="./assets/images/mobile_images/aenean-slider-img1.png"
              alt=""
            />
          </div>
          <div class="slide">
            <img
              src="./assets/images/mobile_images/aenean-slider-img3.png"
              alt=""
            />
          </div>
          <div class="slide">
            <img
              src="./assets/images/mobile_images/aenean-slider-img1.png"
              alt=""
            />
          </div>
          <div class="slide">
            <img
              src="./assets/images/mobile_images/aenean-slider-img1.png"
              alt=""
            />
          </div>
          <template #prevArrow="arrowSlotProps">
            <button
              class="slider-arrow slider-arrow--left"
              @click="arrowSlotProps.onClick"
            >
              <img
                src="./assets/images/mobile_images/slider/slider-arrow-left.png"
                alt="Previous"
              />
            </button>
          </template>
          <template #nextArrow="arrowSlotProps">
            <button
              class="slider-arrow slider-arrow--right"
              @click="arrowSlotProps.onClick"
            >
              <img
                src="./assets/images/mobile_images/slider/slider-arrow-right.png"
                alt="Previous"
              />
            </button>
          </template>
        </VSlickCarousel>
      </div>
      <div class="galleryAenean gallery">
        <img
          src="./assets/images/desktop_images/gallery/aenean-gallery.png"
          alt=""
        />
        <img
          src="./assets/images/desktop_images/gallery/aenean-gallery2.png"
          alt=""
        />
        <img
          src="./assets/images/desktop_images/gallery/aenean-gallery3.png"
          alt=""
        />
      </div>
    </div>
  </section>
  <section class="section-mauris">
    <div class="mauris text">
      <h3 class="text__caption">
        Mauris ultricies ante sit amet ex imperdiet efficitur
      </h3>
      <ul class="text__list">
        <p>
          Proin tempus odio vitae lorem imperdiet, venenatis fermentum ex
          malesuada. Donec justo lacus, rutrum sed viverra at, dignissim sit
          amet enim. Sed id tortor nibh:
        </p>
        <li>
          ⦁ Sed sed dui sit amet massa fermentum lobortis. Nullam iaculis nisi
          quis augue sollicitudin, id vestibulum nisl feugiat. Maecenas tempor
          iaculis lacinia. Quisque in dictum lacus, nec bibendum metus. Sed elit
          dui, maximus sed ex nec, facilisis lacinia ligula. Fusce ut tellus
          luctus, iaculis ex eu, lobortis dolor.
        </li>
        <li>
          Quisque sagittis, ipsum non finibus molestie, nisl risus eleifend
          felis, a cursus sem magna ac massa. Phasellus molestie consectetur
          ornare. Mauris sit amet augue efficitur, posuere massa vitae, tempus
          libero.
        </li>
        <li>
          ⦁ Aliquam erat volutpat. Sed ex ipsum, mattis non pellentesque at,
          efficitur at eros. Integer porttitor tincidunt mi sit amet ornare.
        </li>
        <li>
          ⦁ Proin posuere dolor quis lacus feugiat blandit. Vivamus vitae orci
          in ante malesuada commodo.
        </li>
        <li>
          ⦁ Nam nec bibendum metus, id cursus arcu. Curabitur vel pharetra
          metus, interdum egestas nulla.
        </li>
        <li>
          ⦁ Sed ipsum lacus, auctor vel nisi et, interdum rhoncus nunc. Mauris
          ultricies ante sit amet ex imperdiet efficitur.
        </li>
        <li>
          ⦁ Fusce sed odio posuere, laoreet orci ac, rutrum nisl. Sed vel
          molestie neque, aliquam cursus turpis!
        </li>
      </ul>
      <div class="comp__hero2">
        <Hero
          :caption="heroData2.caption"
          :lemon="heroData2.lemon"
          :img1="heroData2.img1"
          :img2="heroData2.img2"
          img3=""
        />
      </div>
    </div>
  </section>
  <section class="section-donec">
    <div class="donec text">
      <h3 class="text__caption">
        Donec mi ex efficitur fringilla laoreet eget
      </h3>
      <ul class="text__list">
        <p>
          Maecenas convallis pulvinar eros, vitae dictum lacus pellentesque vel.
          Integer faucibus commodo neque, in pretium mauris accumsan in. Sed sed
          felis in nunc faucibus maximus. Integer mollis facilisis nunc ut
          hendrerit. Donec ante metus, tristique non consectetur id, commodo
          eget dolor.
        </p>
        <li>
          ⦁ Aenean ac vehicula libero. Curabitur faucibus velit quam, ut
          volutpat enim finibus in. Nam ultrices fermentum ultrices. Sed leo
          tellus, pellentesque hendrerit imperdiet et, viverra ut nunc. Donec
          lobortis vitae mauris vitae pretium. Donec mi ex, efficitur fringilla
          laoreet eget, aliquam vel quam.
        </li>
        <li>
          ⦁ Integer faucibus commodo neque, in pretium mauris accumsan in. Sed
          sed felis in nunc faucibus maximus.
        </li>
        <li>
          ⦁ Morbi nec quam lacus. Maecenas convallis pulvinar eros, vitae dictum
          lacus pellentesque vel.
        </li>
        <span>Aliquam id porttitor: </span>
        <li>
          ⦁ Praesent mauris ipsum, aliquam a justo nec, sodales vulputate sem.
          Nullam ac ante leo. Fusce viverra lectus dignissim condimentum
          hendrerit.
        </li>
        <li>
          ⦁ Sed quis enim in dui congue eleifend. Nunc interdum risus sit amet
          scelerisque eleifend. Pellentesque erat diam, mattis a felis in,
          finibus consectetur elit. Donec semper sed vestibulum.
        </li>
        <li>
          ⦁ Mauris molestie, velit nec semper tincidunt, magna diam blandit
          quam, vitae pharetra sapien dui at justo. Nulla in nisi nulla. Aenean
          pulvinar pulvinar scelerisque.
        </li>
        <li>
          ⦁ Vivamus condimentum ullamcorper ipsum, ac elementum justo semper
          eget. Pellentesque luctus at ex ut hendrerit. Proin bibendum faucibus
          lacinia. Aenean quis ex ac risus lobortis interdum sit amet nec quam.
          Integer consectetur mi nunc, et vestibulum metus tempor ac.
        </li>
      </ul>
    </div>
    <div class="donec__slider">
      <Slider />
    </div>
    <div class="donec__gallery">
      <img src="../src/assets/images/mobile_images/slider/1.png" alt="" />
      <img src="../src/assets/images/mobile_images/slider/2.png" alt="" />
      <img src="../src/assets/images/mobile_images/slider/3.png" alt="" />
      <img src="../src/assets/images/mobile_images/slider/4.png" alt="" />
      <img src="../src/assets/images/mobile_images/slider/5.png" alt="" />
      <img src="../src/assets/images/mobile_images/slider/6.png" alt="" />
      <img src="../src/assets/images/mobile_images/slider/7.png" alt="" />
    </div>
    <div class="gallery">
      <img src="./assets/images/desktop_images/gallery/1.png" alt="" />
      <img src="./assets/images/desktop_images/gallery/2.png" alt="" />
      <img src="./assets/images/desktop_images/gallery/3.png" alt="" />
      <img src="./assets/images/desktop_images/gallery/4.png" alt="" />
      <img src="./assets/images/desktop_images/gallery/5.png" alt="" />
      <img src="./assets/images/desktop_images/gallery/6.png" alt="" />
      <img src="./assets/images/desktop_images/gallery/7.png" alt="" />
    </div>
  </section>
  <section class="section-vestibulum">
    <div class="vestibulum text">
      <h3 class="text__caption">Vestibulum vitae enim tellus</h3>
      <ul class="text__list">
        <p>
          Mauris nec mi egestas, lacinia purus vitae, luctus ligula. Lorem ipsum
          dolor sit amet, consectetur adipiscing elit.
        </p>
        <li>
          ⦁ Maecenas posuere semper sem, in blandit mauris luctus a.
          Pellentesque placerat pulvinar est, at pretium leo lobortis nec. Nunc
          elementum tristique maximus. Quisque nec neque dictum, scelerisque
          turpis ac, tempor erat.
        </li>
        <li>
          ⦁ Aenean quis massa id purus venenatis fringilla ac id nisl. Cras nec
          dapibus turpis. Integer sit amet consequat lectus. Donec laoreet
          accumsan faucibus. Cras vehicula lobortis aliquam. Phasellus posuere
          pretium lorem scelerisque auctor.
        </li>
      </ul>
      <div class="vestibulum__slider">
        <VSlickCarousel v-bind="settings2">
          <div class="tema tema2">
            <div class="slider-item slider-item2">
              <div>
                <img
                  src="./assets/images/mobile_images/slider/border-image1.png"
                  alt="slider image 1"
                />
              </div>
              <div>
                <img
                  src="./assets/images/mobile_images/slider/border-image2.png"
                  alt="slider image 2"
                />
              </div>
            </div>
          </div>
          <div class="tema tema2">
            <div class="slider-item slider-item2">
              <div>
                <img
                  src="./assets/images/mobile_images/slider/border-image1.png"
                  alt="slider image 1"
                />
              </div>
              <div>
                <img
                  src="./assets/images/mobile_images/slider/border-image2.png"
                  alt="slider image 2"
                />
              </div>
            </div>
          </div>
          <template #prevArrow="arrowSlotProps">
            <button
              class="slider-arrow slider-arrow--left"
              @click="arrowSlotProps.onClick"
            >
              <img
                src="./assets/images/mobile_images/slider/slider-arrow-left.png"
                alt="Previous"
              />
            </button>
          </template>
          <template #nextArrow="arrowSlotProps">
            <button
              class="slider-arrow slider-arrow--right"
              @click="arrowSlotProps.onClick"
            >
              <img
                src="./assets/images/mobile_images/slider/slider-arrow-right.png"
                alt="Previous"
              />
            </button>
          </template>
        </VSlickCarousel>
      </div>
      <div class="vestibulum__slider2">
        <VSlickCarousel v-bind="settings2">
          <div class="tema tema2">
            <div class="slider-item slider-item2">
              <div>
                <img
                  src="./assets/images/mobile_images/slider/border-image1.png"
                  alt="slider image 1"
                />
              </div>
              <div>
                <img
                  src="./assets/images/mobile_images/slider/border-image2.png"
                  alt="slider image 2"
                />
              </div>
              <div>
                <img
                  src="./assets/images/mobile_images/slider/border-image1.png"
                  alt="slider image 1"
                />
              </div>
            </div>
          </div>
          <div class="tema tema2">
            <div class="slider-item slider-item2">
              <div>
                <img
                  src="./assets/images/mobile_images/slider/border-image1.png"
                  alt="slider image 1"
                />
              </div>
              <div>
                <img
                  src="./assets/images/mobile_images/slider/border-image2.png"
                  alt="slider image 2"
                />
              </div>
              <div>
                <img
                  src="./assets/images/mobile_images/slider/border-image1.png"
                  alt="slider image 1"
                />
              </div>
            </div>
          </div>
          <template #prevArrow="arrowSlotProps">
            <button
              class="slider-arrow slider-arrow--left"
              @click="arrowSlotProps.onClick"
            >
              <img
                src="./assets/images/mobile_images/slider/slider-arrow-left.png"
                alt="Previous"
              />
            </button>
          </template>
          <template #nextArrow="arrowSlotProps">
            <button
              class="slider-arrow slider-arrow--right"
              @click="arrowSlotProps.onClick"
            >
              <img
                src="./assets/images/mobile_images/slider/slider-arrow-right.png"
                alt="Previous"
              />
            </button>
          </template>
        </VSlickCarousel>
      </div>
      <div class="vestibulum__gallery gallery">
        <img
          src="./assets/images/desktop_images/gallery/vestibulum-gallery.png"
          alt=""
        />
        <img
          src="./assets/images/desktop_images/gallery/vestibulum-gallery2.png"
          alt=""
        />
        <img
          src="./assets/images/desktop_images/gallery/vestibulum-gallery3.png"
          alt=""
        />
        <img
          src="./assets/images/desktop_images/gallery/vestibulum-gallery4.png"
          alt=""
        />
      </div>
    </div>
  </section>
  <section class="section-etiam">
    <div class="etiam text">
      <h3 class="text__caption etiam__caption">
        Etiam malesuada suscipit eleifend. Integer malesuada
      </h3>
      <ul class="text__list">
        <p>
          Sed varius, odio eu feugiat mollis, risus nunc scelerisque leo, eu
          auctor neque ipsum eu turpis. Sed efficitur mauris sit amet nulla
          porta, quis tempus nisi lobortis. Etiam malesuada suscipit eleifend.
          Integer malesuada orci ante, porttitor eleifend nisl dignissim in.
        </p>
        <span>Quisque malesuada purus et sagittis tempus: </span>
        <li>
          ⦁ Etiam sed faucibus eros. Aenean nisi augue, consectetur quis sodales
          non, pharetra sed orci.
        </li>
        <li>
          ⦁ Nunc pellentesque ipsum eget ligula hendrerit, sed commodo arcu
          semper.
        </li>
        <li>
          ⦁ Nunc et nulla sagittis dui dignissim mattis at sit amet ex. In hac
          habitasse platea dictumst. Ut tempus elementum nulla et eleifend.
          Morbi eget leo massa. Donec aliquam orci a nulla ornare aliquam. In
          cursus faucibus ultricies. Vestibulum semper lacinia ipsum, sed ornare
          eros dignissim sed.
        </li>
      </ul>
      <div class="comp__hero3">
        <Hero
          :caption="heroData3.caption"
          :lemon="heroData3.lemon"
          :img1="heroData3.img1"
          :img2="heroData3.img2"
          :img3="heroData3.img3"
        />
      </div>
    </div>
  </section>
  <section class="section-reviews">
    <Reviews />
  </section>
  <section class="section-cursus">
    <div class="cursus text">
      <h3 class="text__caption">In cursus faucibus ultricies</h3>
      <ul class="text__list">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus
          ornare purus non orci suscipit, vitae posuere magna eleifend. Fusce
          cursus sed dui et volutpat. Donec suscipit sodales arcu, eu aliquam
          lectus convallis eget. Sed luctus nec tellus at luctus. Aliquam purus
          orci, cursus sed hendrerit sit amet, tincidunt eget nibh. Proin
          pulvinar nunc id tortor feugiat eleifend. Quisque nec consectetur leo,
          et blandit nisi. Maecenas ac libero eget elit gravida blandit. Vivamus
          tempor imperdiet nisl a vestibulum. Duis gravida sodales nisi nec
          pellentesque. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
          Vivamus ornare purus non orci suscipit, vitae posuere magna eleifend.
        </p>
      </ul>
      <div class="carousel">
        <VSlickCarousel v-bind="settings">
          <div class="slide">
            <img src="./assets/images/mobile_images/cursus-slider.png" alt="" />
          </div>
          <div class="slide">
            <img src="./assets/images/mobile_images/cursus-slider.png" alt="" />
          </div>
          <div class="slide">
            <img src="./assets/images/mobile_images/cursus-slider.png" alt="" />
          </div>
          <div class="slide">
            <img src="./assets/images/mobile_images/cursus-slider.png" alt="" />
          </div>
          <template #prevArrow="arrowSlotProps">
            <button
              class="slider-arrow slider-arrow--left"
              @click="arrowSlotProps.onClick"
            >
              <img
                src="./assets/images/mobile_images/slider/slider-arrow-left.png"
                alt="Previous"
              />
            </button>
          </template>
          <template #nextArrow="arrowSlotProps">
            <button
              class="slider-arrow slider-arrow--right"
              @click="arrowSlotProps.onClick"
            >
              <img
                src="./assets/images/mobile_images/slider/slider-arrow-right.png"
                alt="Previous"
              />
            </button>
          </template>
        </VSlickCarousel>
      </div>
      <div class="galleryCursus gallery">
        <img
          src="./assets/images/desktop_images/gallery/cursus-gallery.png"
          alt=""
        />
        <img
          src="./assets/images/desktop_images/gallery/cursus-gallery2.png"
          alt=""
        />
        <img
          src="./assets/images/desktop_images/gallery/cursus-gallery3.png"
          alt=""
        />
      </div>
      <h3 class="text__caption">Vestibulum auctor libero massa</h3>
      <ul class="text__list text__list--bottom">
        <p>
          Aenean quis nibh massa. In hac habitasse platea dictumst. Aenean
          commodo metus quis malesuada sollicitudin. Vestibulum molestie velit
          non erat gravida pulvinar. Mauris vehicula at orci at venenatis. Donec
          tincidunt augue ut scelerisque viverra. Vivamus blandit mi tempus
          tristique tempor. Fusce tempor maximus facilisis. Proin aliquet dolor
          id mi faucibus dapibus. Pellentesque vitae enim eu ex feugiat
          bibendum. Sed iaculis, augue eu efficitur varius, tortor nulla
          porttitor ipsum, nec imperdiet justo erat in diam. Nulla eu efficitur
          neque, vel faucibus diam. Duis consequat id lacus ac dictum. In ligula
          arcu, fringilla dignissim feugiat sed, hendrerit ac justo. Cras
          pretium turpis ut eleifend euismod. Duis congue venenatis massa, sit
          amet congue tellus volutpat quis. Nulla ultrices iaculis vestibulum.
          Donec vel est sed odio rhoncus mattis at nec urna.
        </p>
      </ul>
    </div>
  </section>
  <Accordion />
  <section class="section-footer">
    <Footer />
  </section>
</template>

<style lang="scss">
.comp__hero1 {
  margin-bottom: 58px;
  .hero__img--arrow {
    display: none;
  }
}
.comp__hero2 {
  .hero__img--top {
    top: -40px;
    right: 10px;
  }
  .hero__img--bottom {
    right: 22px;
    bottom: -45px;
  }
  .hero__img--arrow {
    display: none;
  }
}
.comp__hero3 {
  .hero-container {
    padding: 46px 0px 46px 28px;
  }
  img {
    position: absolute;
  }
  .hero__img--top {
    top: -42px;
    right: 80px;
  }
  .hero__img--arrow {
    top: 0px;
    right: 15px;
  }
  .hero__img--bottom {
    bottom: -28px;
    right: -14px;
  }
  .hero__caption--gray {
    display: none;
  }
}
.gallery {
  display: none;
}
.section-content,
.section-donec,
.section-etiam {
  margin-bottom: 30px;
}

.caption {
  font-size: 20px;
  line-height: 29.64px;
}
.content {
  &__caption {
    margin-bottom: 16px;
  }

  &__text {
    margin-bottom: 30px;
  }
}
.container {
  margin-bottom: 22px;
}
.section-aenean {
  margin-bottom: 22px;
  .aenean {
    &__caption {
      margin-bottom: 15px;
    }
  }
}
.donec__slider {
  display: none;
}
.vestibulum__slider2 {
  display: none;
}
.carousel {
  .slide {
    margin-bottom: 60px;
    img {
      width: -webkit-fill-available;
    }
  }
}
.section-mauris {
  margin-bottom: 34px;
}
.text__caption {
  margin-bottom: 15px;
}
.text__list {
  margin-bottom: 30px;
  font-size: 14px;
  line-height: 20.75px;
  list-style: none;
  display: flex;
  flex-direction: column;
  padding: 0;
  span {
    font-weight: 700;
  }
  li {
    font-weight: 400;
  }
}

.donec {
  &__gallery {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    row-gap: 7px;
    column-gap: 11px;
  }
}

.tema2 {
  display: flex;
  margin-bottom: 150px;
}
.section-vestibulum {
  margin-bottom: 22px;
}
.slider-item2 {
  display: flex;
  gap: 16px;
  img {
    width: 162px;
    height: 243px;
  }
}
.etiam__caption {
  max-width: 322px;
}
.section-reviews {
  margin-bottom: 30px;
}
.section-cursus {
  .carousel {
    margin-bottom: 22px;
  }
}
.section-footer {
  display: none;
}
@media screen and (min-width: 600px) {
  .section-content,
  .section-donec,
  .section-etiam,
  .section-aenean {
    margin-bottom: 50px;
  }
  .text__caption,
  .caption {
    font-size: 25px;
    line-height: normal;
    margin-bottom: 30px;
  }

  .content {
    &__text {
      font-size: 18px;
      margin-bottom: 50px;
    }
  }
  .container {
    margin-bottom: 50px;
  }
  .text__list {
    font-size: 18px;
    margin-bottom: 50px;
    span {
      font-weight: 400;
    }
  }
  .etiam {
    .text__list {
      margin-bottom: 120px;
    }
  }
  .carouselAenean {
    .v-slick-track {
      margin-bottom: 50px;
      img {
        width: 97%;
      }
    }
  }
}
@media screen and (min-width: 767px) {
  .donec__slider {
    .slider-item {
      img {
        min-height: 210px;
        min-width: 164px;
      }
    }
    display: block;
  }
  .donec__gallery {
    display: none;
  }
  .vestibulum__slider {
    display: none;
  }
  .vestibulum__slider2 {
    .slider-item {
      img {
        width: 200px;
        height: 310px;
      }
      margin-bottom: 100px;
    }
    display: block;
  }
}
@media screen and (min-width: 1024px) {
  .carousel2 {
    display: none;
  }
  .gallery {
    display: flex;
    justify-content: space-between;
    margin: 0 auto;
    img {
      flex-grow: 1;
      flex-shrink: 1;
      min-width: 100px;
      max-width: 288px;
      height: auto;
    }
  }
  .carouselAenean {
    display: none;
  }
  .galleryAenean {
    img {
      min-width: 300px;
      max-width: 533px;
    }
  }
  .vestibulum__slider2 {
    display: none;
  }
  .section-cursus {
    .carousel {
      display: none;
    }
  }
}
@media screen and (min-width: 1440px) {
  .caption,
  .text__caption {
    font-size: 48px;
    margin-bottom: unset;
  }
  .content__text,
  .text__list {
    font-size: 24px;
    line-height: normal;
    margin-bottom: 30px;
  }
  .section-content {
    .comp__hero1 {
      margin-bottom: 5px;
    }
  }

  .section-aenean {
    .text__list {
      span {
        font-size: 36px;
      }
    }
  }
  .section-etiam {
    .text__list {
      margin-bottom: 90px;
    }
    .etiam__caption {
      max-width: unset;
    }
  }
  .section-cursus {
    .text__list {
      margin-bottom: 50px;
      &--bottom {
        margin-bottom: 150px;
      }
    }
    .galleryCursus {
      margin-bottom: 50px;
      img {
        min-width: 410px;
      }
    }
  }
  .section-footer {
    position: relative;
    z-index: 1;
    background: #361039;
    display: block;
    padding: 0;
  }
  .section-footer::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(
      180deg,
      rgba(154, 56, 180, 0.2) 0%,
      rgba(109, 17, 133, 0) 100%
    );
    z-index: -1;
  }
}
</style>
