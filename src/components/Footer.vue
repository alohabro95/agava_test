<script></script>
<template>
  <div class="footer">
    <div class="columns">
      <div class="columns__el">
        <span class="columns__caption">Lorem Ipsum</span>
        <ul class="columns__list columns__list--1">
          <li>Nam sit</li>
          <li>Pellentesque</li>
          <li>Ut vitae</li>
          <li>Sitemap</li>
        </ul>
        <div class="columns__spans">
          <span class="columns__caption">Donec nunc </span>
          <span class="columns__caption">Nulla facilisi</span>
        </div>
      </div>
      <div class="columns__el">
        <span class="columns__caption">Interdum</span>
        <ul class="columns__list">
          <li>Nullam</li>
          <li>Mauris</li>
          <li>Fusce</li>
          <li>Pellentesque</li>
          <li>Aliquam</li>
          <li>Curabitur non</li>
          <li>Fermentum</li>
          <li>Viverra sapien</li>
        </ul>
      </div>
      <div class="columns__el">
        <span class="columns__caption">Cras porta</span>
        <ul class="columns__list">
          <li>Malesuada</li>
          <li>Quisque nec</li>
          <li>Etiam at porta</li>
          <li>Lobortis</li>
          <li>Tincidunt tellus</li>
          <li>Rhoncus est</li>
          <li>Feugiat ligula</li>
          <li>Bibendum</li>
          <li>Vestibulum</li>
        </ul>
      </div>
      <div class="columns__el">
        <span class="columns__caption">Duis semper</span>
        <ul class="columns__list">
          <li>Prelia minour</li>
          <li>Prelia benden</li>
          <li>Mauris</li>
          <li>Duis consequat</li>
          <li>Curabitur egestas</li>
        </ul>
      </div>
      <div class="columns__el">
        <span class="columns__caption">Cras dignissim</span>
        <ul class="columns__list">
          <li>Dapibus quis</li>
          <li>Vel mauris</li>
          <li>Habitant</li>
          <li>Commodo</li>
          <li>Dictum</li>
          <li>Tristique</li>
          <li>Et malesuada</li>
          <li>Sollicitudin</li>
          <li>Tempus magna</li>
          <li>Sed fringilla</li>
        </ul>
      </div>
      <div class="columns__el">
        <span class="columns__caption">Lorem ipsum dolor</span>
        <ul class="columns__list columns__list--6">
          <li>Pellentesque eu consequat</li>
          <li>Quisque luctus</li>
          <li>Mauris porttitor</li>
        </ul>
        <span class="columns__caption">Vivamus ornare</span>
      </div>
      <div class="columns__el">
        <span class="columns__caption">Duis minar </span>
        <ul class="columns__list">
          <li>Ipsum primis</li>
          <li>Joygri minas</li>
          <li>Olleni cristos</li>
          <li>Leo</li>
          <li>Gravida</li>
          <li>Auctor</li>
        </ul>
      </div>
    </div>
    <div class="logos">
      <img src="../assets/images/desktop_images/footer/1.png" alt="" />
      <img src="../assets/images/desktop_images/footer/2.png" alt="" />
      <img src="../assets/images/desktop_images/footer/3.png" alt="" />
      <img src="../assets/images/desktop_images/footer/4.png" alt="" />
      <img src="../assets/images/desktop_images/footer/5.png" alt="" />
      <img src="../assets/images/desktop_images/footer/6.png" alt="" />
      <img src="../assets/images/desktop_images/footer/7.png" alt="" />
    </div>
    <div class="footer__text">
      <span
        >Nam euismod, lacus nec commodo commodo, tortor lacus laoreet enim, eget
        congue velit neque vel urna.</span
      >
      <span>Curabitur sit amet erat id leo porttitor ultricies.</span>
    </div>
  </div>
</template>
<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap");
.footer {
  padding: 100px 80px 165px 80px;
  span,
  li {
    font-family: "Montserrat", sans-serif;
  }
  &__text {
    font-size: 27px;
    display: flex;
    flex-direction: column;
    text-align: center;
  }
}
.columns {
  display: flex;
  justify-content: space-between;
  font-size: 17px;
  margin-bottom: 135px;
  &__el,
  &__list,
  &__spans {
    display: flex;
    flex-direction: column;
  }

  &__el {
    gap: 40px;
  }

  &__caption {
    color: #d536ff;
    font-weight: 700;
  }

  &__list {
    gap: 36px;
    list-style: none;
    &--1 {
      margin-bottom: 52px;
    }
    &--6 {
      margin-bottom: 50px;
    }
  }

  &__spans {
    gap: 36px;
  }
}
.logos {
  display: flex;
  width: fit-content;
  margin: 0 auto;
  gap: 55px;
  margin-bottom: 90px;
}
</style>
