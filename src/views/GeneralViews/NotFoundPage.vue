<template>
  <div>
    <!-- Header -->
    <div class="header bg-gradient-info py-7 py-lg-8 pt-lg-9">
      <div class="container">
        <div class="header-body text-center mb-7">
          <div class="row justify-content-center">
            <div class="col-xl-5 col-lg-6 col-md-8 px-5">
              <h1 class="text-light">Упс!</h1>
              <p class="text-lead text-white">Страница не найдена. Не волнуйтесь, у нас есть много других страниц для изучения</p>

              <router-link to="/alternative" class="font-weight-bold text-white mt-5">Назад к панели</router-link>
            </div>
          </div>
        </div>
      </div>
      <div class="separator separator-bottom separator-skew zindex-100">
        <svg x="0" y="0" viewBox="0 0 2560 100" preserveAspectRatio="none" version="1.1" xmlns="http://www.w3.org/2000/svg">
          <polygon class="fill-default" points="2560 0 2560 100 0 100"></polygon>
        </svg>
      </div>
    </div>
    <!-- Page content -->
    <!-- <section class="py-6">
      <div class="container">
        <div class="row row-grid align-items-center">
          <div class="col-md-6">
            <img src="/img/theme/landing-2.png" class="img-fluid">
          </div>
          <div class="col-md-6">
            <div class="pr-md-5">
              <h1 class="text-light">Исследуйте страницы</h1>
              <p class="text-light">If you want to get inspiration or just show something directly to your clients, you can jump start your development with our pre-built example pages.</p>
              <router-link to="/pages/user" class="font-weight-bold text-warning mt-5">Explore pages</router-link>
            </div>
          </div>
        </div>
      </div>
    </section> -->
  </div>
</template>

<script>

export default {
  name: 'not-found'
};
</script>
