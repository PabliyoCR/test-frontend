<template lang="pug">

q-header(elevated)
  q-toolbar(:class="{ 'tools' : $q.screen.gt.xs, 'tools-m' : !$q.screen.gt.xs}")
    img(src="~assets/logo.svg" width="150")
    q-space
    q-tabs.gt-xs(inline-label shrink indicator-color="transparent")
      q-tab(icon = "fas fa-square-full" name="a" label = "Duis vestibulum" class="toolbarTab" no-caps @click = "goTo('section-2')")
      q-tab(icon = "fas fa-square-full" name="b" label = "Phasellus consequat" class="toolbarTab" no-caps @click = "goTo('section-3')")
      q-tab(icon = "fas fa-square-full" name="c" label = "Donec sit amet lectus" class="toolbarTab" no-caps @click = "goTo('section-4')")
    .lt-sm.panel-m
      q-icon.q-mr-md.cursor-pointer(name = "fas fa-square-full" style="padding: 0" @click = "goTo('section-1')" :class="{ 'viewport-m' : current_section == 'section-1'}")
      q-icon.q-mr-md.cursor-pointer(name = "fas fa-square-full" style="padding: 0" @click = "goTo('section-2')" :class="{ 'viewport-m' : current_section == 'section-2'}")
      b.q-mr-md.cursor-pointer(@click = "goTo('section-3')" style="font-size: 10pt" :class="{ 'viewport-m' : current_section == 'section-3'}") ₡
      q-icon.cursor-pointer(name = "fas fa-square-full" style="padding: 0" @click = "goTo('section-4')" :class="{ 'viewport-m' : current_section == 'section-4'}")

#section-1(v-intersection="onIntersection" style="position: relative;")
  h1(:class="{ 'titulo' : $q.screen.gt.xs, 'titulo-m' : !$q.screen.gt.xs}") Lorem Ipsum dolor sit amet
  h2(:class="{ 'subtitulo' : $q.screen.gt.xs, 'subtitulo-m' : !$q.screen.gt.xs}")
    span(style="font-family: 'customfont-sans-semi-bold'") Lorem 
    | Ipsum is simply dummy text.
  .row
    q-btn.customButton(unelevated no-caps :class="{ 'customButton-1' : $q.screen.gt.xs, 'customButton-1-m' : !$q.screen.gt.xs}")
      .customButtonContent Donec velita
      q-icon.q-pl-md(name = "fas fa-caret-right")
  .row.gt-xs
    q-btn.customButton.customButton-1(unelevated no-caps)
      .customButtonContentItalic Nulla quis velit molestie
      q-icon.q-pl-md(name = "fas fa-caret-right")
  .row.gt-xs
    q-btn.blandit(unelevated no-caps  @click = "goTo('section-2')")
      div
        div(style="font-family: 'customfont-sans-light'") blandit purus
        img.q-mt-sm(src="~assets/shevron-down.svg" width="50")
  .row.sm(style="padding: 5em")
  .gt-xs(style="z-index:-1; width: 100%; height: 100%; position: absolute; top: 0; left: 0; background-image: url('assets/background-1.svg'); background-repeat: no-repeat; background-position: bottom right; background-size: 500px;")
    div(style="color: white; z-index:-1; position: absolute; bottom: 45px; right: 300px;") Phasellus consequat ru 
      br
      | trum ante eget aliqua.*
      q-icon(name = "fas fa-caret-right")
  .lt-sm(style="z-index:-1; width: 100%; height: 100%; position: absolute; top: 0; left: 0; background-image: url('assets/background-2.svg'); background-repeat: no-repeat; background-position: bottom right; background-size: 300px;")
    div(style="font-size: 12px; color: white; z-index:-1; position: absolute; bottom: 23px; right: 150px;") Phasellus consequat ru 
      br
      | trum ante eget aliqua.*
      q-icon(name = "fas fa-caret-right")
  
.background-secundario
  div(:class="{ 'texto-2' : $q.screen.gt.xs, 'texto-2-m' : !$q.screen.gt.xs}")
    span.gt-xs(style="font-size:24px") Lorem Ipsum, 
    span.lt-sm(style="font-size:16px") Lorem Ipsum, 
    | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam posuere odio orci. 
    .q-pt-md(style="font-family: 'customfont-sans-light';") Duis vestibulum ultricies leo, nec dapibus ligula luctus ut. In dapibus dui ac erat lobortis pulvinar. Fusce a arcu tempor, feugiat odio et, varius enim.
    .q-pt-md.gt-xs(style="font-family: 'customfont-sans-bold'; font-size:15px") Phasellus consequat rutrum ante eget aliquam.
    .q-pt-md.lt-sm(style="font-family: 'customfont-sans-bold'; font-size:18px") Phasellus consequat rutrum ante eget aliquam.

#section-2.texto(v-intersection="onIntersection" :class="{ 'contenedor' : $q.screen.gt.xs, 'contenedor-m' : !$q.screen.gt.xs}")
  h1(:class="{ 'titulo-2' : $q.screen.gt.xs, 'titulo-2-m' : !$q.screen.gt.xs}") Duis vestibulum, nec dapibus ligula
  h2.q-pt-sm(:class="{ 'subtitulo-2' : $q.screen.gt.xs, 'subtitulo-2-m' : !$q.screen.gt.xs}") In dapibus dui ac erat lobortis.
  div.q-pt-lg Nulla quis velit molestie, congue leo ac, bibendum dui. Pellentesque ut sem vel metus ornare aliquam vel ut neque. Suspendisse ac ipsum nec ipsum ultricies porta. Praesent ut ornare lacus.
  .row.card-1
    .col-md-4.q-pt-md.q-pr-xl
      .texto(style="font-size : 21px; color :  #27A549") Fusce a arcu
      svg(width="100%" height="10")
        rect(width="100%" height="10" style="fill : #27A549;")
      .q-pt-md Feugiat odio et, varius enim. Sed eleifend ex et auctor lacinia. Fusce in efficitur lorem. Donec blandit urna et dolor ultrices pellentesque. 
    .col-md-4.q-pt-md.q-pr-xl
      .texto(style="font-size : 21px; color :  #106839") Nulla quis velit
      svg(width="100%" height="10")
        rect(width="100%" height="10" style="fill : #106839;")
      .q-pt-md Molestie, congue leo ac, bibendum dui. Pellentesque ut sem vel metus ornare aliquam vel ut neque. 
    .col-md-4.q-pt-md
      .texto(style="font-size : 21px; color :  #8EC544") Pellentesque ut sem
      svg(width="100%" height="10")
        rect(width="100%" height="10" style="fill : #8EC544;")
      .q-pt-md Vel metus ornare aliquam vel ut neque. Suspendisse ac ipsum nec ipsum ultricies porta. Praesent ut ornare lacus.  Pellentesque non tortor vel erat feugiat.
  .row.q-pt-lg.q-pb-sm
    .remark Fusce in efficitur 
      span.custom-green-2 555-555-5555 
      | Curabitur viverra, molestie tincidunt.

  .row.q-mt-sm
    q-btn.customButton.q-mr-xl(unelevated no-caps)
      .customButtonContent Donec velita
      q-icon.q-pl-md(name = "fas fa-caret-right")
    q-btn.gt-xs.customButton(unelevated no-caps)
      .customButtonContentItalic Nulla quis velit molestie
      q-icon.q-pl-md(name = "fas fa-caret-right")

  .row.q-mt-lg
    div(style="font-size : 11px") Duis vestibulum ultricies leo, nec dapibus ligula luctus ut. In dapibus dui ac erat lobortis pulvinar. Fusce a arcu tempor, feugiat odio et, varius enim. Nulla quis velit molestie, congue leo ac, bibendum dui. Pellentesque ut sem vel metus ornare aliquam vel ut neque. Suspendisse ac ipsum nec ipsum ultricies porta. Praesent ut ornare lacus. Pellentesque non tortor vel erat feugiat elementum.

img.gt-xs(src="~assets/separador-1.svg")
img.lt-sm(src="~assets/separador-2.svg")

#section-3.texto(v-intersection="onIntersection" :class="{ 'contenedor' : $q.screen.gt.xs, 'contenedor-m' : !$q.screen.gt.xs}")
  h1(:class="{ 'titulo-2' : $q.screen.gt.xs, 'titulo-2-m' : !$q.screen.gt.xs}" style = "font-family: 'customfont-sans-semi-bold'") Phasellus conse
  div.q-pt-md Duis vestibulum ultricies leo, nec dapibus ligula luctus ut. In dapibus dui ac erat lobortis pulvinar. Fusce a arcu tempor, feugiat odio et, varius enim. Nulla quis velit molestie, congue leo ac, bibendum dui. Pellentesque ut sem vel metus ornare aliquam vel ut neque. Suspendisse ac ipsum nec ipsum ultricies porta.
  .row(style="text-align: center;" :class="{ 'card-2' : $q.screen.gt.xs}")
    .col-md-4.q-pt-md.q-pr-sm
      .row
        .col.q-pr-xs
          .texto.precio(style="color : #106839") ₡2,500
          svg(width="100%" height="10")
            rect(width="100%" height="10" style="fill : #106839;")
          .precio-detalle(style="background-color: #DBE8E1") Donecandit 
            br
            | ₡1,000,000+
        .col
          .texto.precio(style="color : #106839") ₡1,200
          svg(width="100%" height="10")
            rect(width="100%" height="10" style="fill : #106839;")
          .precio-detalle(style="background-color: #DBE8E1") Donecandit 
            br 
            | ₡500K - ₡999,999
    .col-md-4.q-pt-md.q-pr-sm
      .row
        .col.q-pr-xs
          .texto.precio(style="color : #27A549") ₡600
          svg(width="100%" height="10")
            rect(width="100%" height="10" style="fill : #27A549;")
          .precio-detalle(style="background-color: #DFF2E4") Donecandit 
            br
            | ₡250K - ₡499,999
        .col
          .texto.precio(style="color : #27A549") ₡300
          svg(width="100%" height="10")
            rect(width="100%" height="10" style="fill : #27A549;")
          .precio-detalle(style="background-color: #DFF2E4") Donecandit 
            br
            | ₡100K - ₡249,999
    .col-md-4.q-pt-md.q-pr-sm
      .row
        .col.q-pr-xs
          .texto.precio(style="color : #8EC544") ₡200
          svg(width="100%" height="10")
            rect(width="100%" height="10" style="fill : #8EC544;")
          .precio-detalle(style="background-color: #EEF6E3") Donecandit 
            br
            | ₡50K - ₡99,999
        .col
          .texto.precio(style="color : #8EC544") ₡100
          svg(width="100%" height="10")
            rect(width="100%" height="10" style="fill : #8EC544;")
          .precio-detalle(style="background-color: #EEF6E3") Donecandit 
            br
            | ₡25K - ₡49,999

  .q-pt-lg Donec sit amet lectus elementum, mollis odio eu, blandit purus. In iaculis sapien eu vestibulum eleifend.
  
  .row.q-pt-md.q-pb-sm
    .remark Donec eu ante erat. Vivamus iaculis 
      span.custom-green-2 555-555-5555 

  .row.q-mt-md
    q-btn.customButton.q-mr-xl(unelevated no-caps)
      .customButtonContent Donec velita
      q-icon.q-pl-md(name = "fas fa-caret-right")
    q-btn.gt-xs.customButton(unelevated no-caps)
      .customButtonContentItalic Nulla quis velit molestie
      q-icon.q-pl-md(name = "fas fa-caret-right")

img.gt-xs(src="~assets/separador-1.svg")
img.lt-sm(src="~assets/separador-2.svg")

#section-4.texto(v-intersection="onIntersection" :class="{ 'contenedor' : $q.screen.gt.xs, 'contenedor-m' : !$q.screen.gt.xs}")
  h1(:class="{ 'titulo-2' : $q.screen.gt.xs, 'titulo-2-m' : !$q.screen.gt.xs}" style = "font-family: 'customfont-sans-semi-bold'") Donec sit amet
  h2.q-pt-sm(:class="{ 'subtitulo-2' : $q.screen.gt.xs, 'subtitulo-2-m' : !$q.screen.gt.xs}") Curabitur lacinia luctus at justus.
  div.q-pt-md Suspendisse venenatis tempus magna non ultrices. Consectetur In molestie nibh eget 
    br
    a(href="#" style="font-family: 'customfont-sans-semi-bold';") Donec maximus eros mi
  .row
    .col-md-4.q-pr-sm.q-mt-lg
      .card-3(style="height : 100%")
        .texto(style="font-size : 21px; color :  #27A549") Nam dolor massa, vulputate
        svg(width="100%" height="10")
          rect(width="100%" height="10" style="fill : #27A549;")
        .q-pt-md Pellentesque ut sem vel metus ornare aliquam vel ut neque. Suspendisse ac ipsum nec ipsum ultricies porta.
        div.q-py-md.q-pr-lg
          span.remark(style = "font-family: 'customfont-sans-regular'") Falls 
          span.custom-green-2 555-555-5555 
          span.remark(style = "font-family: 'customfont-sans-regular'") au ligula luctus.
        q-btn.customButton(unelevated no-caps)
          .customButtonContent Donec velita
          q-icon.q-pl-md(name = "fas fa-caret-right")
    .col-md-4.q-pr-sm.q-mt-lg
      .card-3(style="height : 100%")
        .texto(style="font-size : 21px; color :  #106839") Sed vestibulum odio sem, sit ametr
        svg(width="100%" height="10")
          rect(width="100%" height="10" style="fill : #106839;")
        .q-py-md Fusce non sodales odio, sit amet dignissim ipsum. Pellentesque eleifend felis augue.
        div(style="font-size : 12px") Sed vitae eros iaculis felis maximus ornare vel egestas tortor. Etiam non rhoncus est, eget fringilla lacus.:
          ul.q-ml-md.q-pr-lg
            li
              a(href="#") Ac, bibendum dui
            li 
              a(href="#") Proin et ultrices turpis Maecenas ultrices
            li 
              a(href="#") Maecenas ique lacinia.
            li Pellentesque ut sem vel metus ornare. 
              q-btn.q-ml-md.question(icon = "fas fa-question" unelevated no-caps @click ="alert = true")
    .col-md-4.q-pr-sm.q-mt-lg
      .card-3(style="height : 100%")
        .texto(style="font-size : 21px; color :  #8EC544") Nullam ac convallis diam, eu prellfua
        svg(width="100%" height="10")
          rect(width="100%" height="10" style="fill : #8EC544;")
        .q-py-md Vivamus vitae urna nisi. Suspendisse ex nunc, ornare eget consectetur sit amet eget consectetur sit amet.
        div(style="font-size : 12px") Phasellus ultrices elit in est imperdiet scelerisque. Aliquam sollicitudin vulputate justo at luctus.
        .q-mt-md
          span.remark(style = "font-family: 'customfont-sans-regular'; font-size: 14px") Falls 
          span.custom-green-2 555-555-555 
          span.remark(style = "font-family: 'customfont-sans-regular'; font-size: 14px") ue non tortor vel erat feugiat elebdrue.

.gt-xs(style = "position: relative;")
  img(src="~assets/separador-3.svg")
  h1.h1-separator Lorem ipsum dolor sit amet, consectetur.

.lt-sm.q-pt-md(style = "background-color : #6CBA48")
  h1.q-mx-md.q-py-lg.h1-separator-m Lorem ipsum dolor sit amet, consectetur.
  img.q-mx-xl(src="~assets/ahorro.svg")

.texto(:class="{ 'footer' : $q.screen.gt.xs, 'footer-m' : !$q.screen.gt.xs}")
  .q-mb-md Duis vestibulum ultricies leo, nec dapibus ligula luctus ut. In dapibus dui ac erat lobortis pulvinar. Fusce a arcu tempor, feugiat odio et, varius enim. Nulla quis velit molestie, congue leo ac, bibendum dui. Pellentesque ut sem vel metus ornare aliquam vel ut neque. Suspendisse ac ipsum nec ipsum ultricies porta. Praesent ut ornare lacus. Pellentesque non tortor vel erat feugiat elementum. 
  .footer-mini-text Donec sit amet lectus elementum, mollis odio eu, blandit purus. In iaculis sapien eu vestibulum eleifend. Praesent lacus nisi, scelerisque et convallis at, tincidunt ut dui. Proin scelerisque aliquam tempus. Suspendisse eleifend metus quis tortor bibendum posuere.
  .footer-mini-text Duis molestie, nibh a porttitor mollis, lorem enim mattis ante, sed placerat arcu ligula id quam. Suspendisse venenatis tempus magna non ultrices. In sagittis felis eget molestie consectetur. In molestie nibh eget diam interdum placerat. Donec maximus eros mi, in pulvinar massa lacinia quis. Praesent a mattis sapien. Nullam sodales nisl congue leo viverra aliquam. Nam ac cursus nibh. Nunc sed sapien id lectus tempor condimentum.
  .footer-mini-text Aliquam tempor nunc sem, sit amet imperdiet ipsum vulputate eget. Donec eu ante erat. Vivamus iaculis dapibus porttitor. Praesent ut mauris dui. Nam dolor massa, vulputate eget libero nec, fringilla fringilla risus. Nam ac nibh nec velit consectetur vestibulum. Ut malesuada tellus vel est dapibus luctus. Sed vestibulum odio sem, sit amet condimentum quam porta maximus. Mauris vulputate orci mauris, at rhoncus felis rhoncus ac. Integer viverra dolor odio, at placerat sem eleifend quis. Nullam ac convallis diam, eu pretium arcu.
  .footer-mini-text Phasellus consequat rutrum ante eget aliquam. Fusce placerat volutpat nibh eget placerat. Nulla id purus vitae nulla ornare aliquet at vel dui. Vivamus vitae urna nisi. Suspendisse ex nunc, ornare eget consectetur sit amet, interdum ut nisi.
  .footer-mini-text Curabitur lacinia, odio quis finibus semper, magna quam faucibus quam, id dictum nibh ligula in diam. Duis molestie, nibh a porttitor mollis, lorem enim mattis ante, sed placerat arcu ligula id quam. Suspendisse venenatis tempus magna non ultrices.
  .footer-mini-text Duis vestibulum ultricies leo, nec dapibus ligula luctus ut. In dapibus dui ac erat lobortis pulvinar. Fusce a arcu tempor, feugiat odio et, varius enim. Nulla quis velit molestie, congue leo ac, bibendum dui. Pellentesque ut sem vel metus ornare aliquam vel ut neque. Suspendisse ac ipsum nec ipsum ultricies porta. Praesent ut ornare lacus. Pellentesque non tortor vel erat feugiat elementum.
  .footer-mini-text Duis vestibulum ultricies leo, nec dapibus ligula luctus ut. In dapibus dui ac erat lobortis pulvinar. Fusce a arcu tempor, feugiat odio et, varius enim. Nulla quis velit molestie, congue leo ac, bibendum dui. Pellentesque ut sem vel metus ornare aliquam vel ut neque. Suspendisse ac ipsum nec ipsum ultricies porta. Praesent ut ornare lacus. Pellentesque non tortor vel erat feugiat elementum.
  .footer-mini-text * Donec sit amet lectus elementum, mollis odio eu, blandit purus. In iaculis sapien eu vestibulum eleifend. Praesent lacus nisi, scelerisque et convallis at, tincidunt ut dui. Proin scelerisque aliquam tempus. Suspendisse eleifend metus quis tortor bibendum posuere. Sed ac cursus tellus. Curabitur lacinia, odio quis finibus semper, magna quam faucibus quam, id dictum nibh ligula in diam. Duis molestie, nibh a porttitor mollis, lorem enim mattis ante, sed placerat arcu ligula id quam. Suspendisse venenatis tempus magna non ultrices. In sagittis felis eget molestie consectetur. In molestie nibh eget diam interdum placerat. Donec maximus eros mi, in pulvinar massa lacinia quis. Praesent a mattis sapien. Nullam sodales nisl congue leo viverra aliquam. Nam ac cursus nibh. Nunc sed sapien id lectus tempor condimentum. Donec sit amet lectus elementum, mollis odio eu, blandit purus. In iaculis sapien eu vestibulum eleifend. Praesent lacus nisi, scelerisque et convallis at, tincidunt ut dui. Proin scelerisque aliquam tempus. Suspendisse eleifend metus quis tortor bibendum posuere. Sed ac cursus tellus. Curabitur lacinia, odio quis finibus semper, magna quam faucibus quam, id dictum nibh ligula in diam. Duis molestie, nibh a porttitor mollis, lorem enim mattis ante, sed placerat arcu ligula id quam. Suspendisse venenatis tempus magna non ultrices. In sagittis felis eget molestie consectetur. In molestie nibh eget diam interdum placerat. Donec maximus eros mi, in pulvinar massa lacinia quis. Praesent a mattis sapien. Nullam sodales nisl congue leo viverra aliquam. Nam ac cursus nibh. Nunc sed sapien id lectus tempor condimentum.

.panel.gt-xs
  .row.q-py-sm.hidden(name="icons_panel")
    q-icon.q-pl-md.cursor-pointer(name = "fas fa-square-full" style="padding: 0" @click = "goTo('section-1')" :class="{ 'viewport' : current_section == 'section-1'}")
  .row.q-py-sm.hidden(name="icons_panel")
    q-icon.q-pl-md.cursor-pointer(name = "fas fa-square-full" style="padding: 0" @click = "goTo('section-2')" :class="{ 'viewport' : current_section == 'section-2'}")
  .row.q-py-sm.hidden(name="icons_panel")
    b.cursor-pointer(@click = "goTo('section-3')" style="font-size: 10pt" :class="{ 'viewport' : current_section == 'section-3'}") ₡
  .row.q-py-sm.hidden(name="icons_panel")
    q-icon.q-pl-md.cursor-pointer(name = "fas fa-square-full" style="padding: 0" @click = "goTo('section-4')" :class="{ 'viewport' : current_section == 'section-4'}")

q-dialog(v-model="alert")
  q-card.alert
    q-card-section 
      .q-pb-sm 1. Donec dictum urna ligula, stibulum lorem lobortis.
      .q-pb-sm 2. Dapibus “Fusce non sodales” Sed vitae eros iaculis felis maximus ornare vel egestas tortor
      .q-pb-sm 3. Praesent ut ornare lacus. Pellentesque non tortor vel erat feugiat.
      .q-py-sm Suspendisse ac ipsum nec ipsum ultricies porta. Praesent ut ornare lacus. Pellentesque non tortor vel erat feugiat elementumPhasellus consequat rutrum.

</template>

<script>
export default {
  data() {
    return {
      current_section: null,
      alert: false,
    };
  },
  methods: {
    goTo(id) {
      const element = document.getElementById(id);
      element.scrollIntoView({ behavior: "smooth" });
    },
    onIntersection(section) {
      if (section.isIntersecting) {
        this.current_section = section.target.id;
      }
    },
  },
  mounted() {
    window.onload = function () {
      const iconos = [...document.getElementsByName("icons_panel")];
      iconos.forEach((el, idx) => {
        setTimeout(() => {
          el.classList.add("anim");
          el.classList.remove("hidden");
          setTimeout(() => {
            el.classList.remove("anim");
          }, 1000);
        }, 500 * idx);
      });
    };
  },
};
</script>
<style lang="sass" scoped>
.contenedor
  padding: 14% 17%

.contenedor-m
  padding: 16% 7%

.titulo
  padding: 7% 16% 0 16%
  font-size: 58pt
  font-family: 'customfont-sans-bold'

.titulo-m
  padding: 8% 7% 0 7%
  font-size: 28pt
  font-family: 'customfont-sans-bold'

.subtitulo
  padding: 2% 30% 2% 16%
  font-size: 36pt
  font-family: 'customfont-sans-regular'

.subtitulo-m
  padding: 2% 7% 2% 7%
  font-size: 18pt
  font-family: 'customfont-sans-regular'

.customButton
  color: white
  background-color: $custom-green-main
  border-radius: 0

.customButton-1
  margin: 0.7em 16%

.customButton-1-m
  margin: 1.5em 7% 11em

.customButtonContent
  font-size: 22px
  font-family: 'customfont-sans-light'

.customButtonContentItalic
  font-size: 22px
  font-family: 'customfont-sans-light-italic'

.blandit
  font-size: 12px
  margin: 4em 0 3em 20%

.texto
  font-family: 'customfont-sans-light'
  font-size: 14px
  line-height: 1.2

.texto-2
  font-family: 'customfont-sans-light'
  font-size: 19px
  line-height: 1.2
  padding: 9% 19% 7% 19%

.texto-2-m
  font-family: 'customfont-sans-light'
  font-size: 15px
  line-height: 1.2
  padding: 24% 8% 16%

.background-secundario
  color: white
  background-color: $custom-green-main

.titulo-2
  font-family: 'customfont-sans-regular'
  font-size: 40pt

.titulo-2-m
  font-family: 'customfont-sans-regular'
  font-size: 26pt

.subtitulo-2
  font-family: 'customfont-sans-regular'
  font-size: 26pt

.subtitulo-2-m
  font-family: 'customfont-sans-regular'
  font-size: 16pt

.card-1
  background-color: $custom-gray-back
  padding: 0 2em 2em 2em
  margin-top: 2em
  margin-left: -2em

.remark
  font-size: 15px
  font-family: 'customfont-sans-semi-bold'
  color: $custom-green-1

.precio
  font-family: 'customfont-sans-regular'
  font-size: 30px

.precio-detalle
  font-family: 'customfont-sans-light'
  font-size: 12px
  padding: 1em 0 1.5em
  margin-top: -0.3em

.card-2
  margin-left: -1em

.card-3
  background-color: $custom-gray-back
  padding: 2em 2em 0.5em 2em

.h1-separator
  color: white
  font-size: 42pt
  font-family: 'customfont-sans-regular'
  position: absolute
  top: 50%
  left: 47%
  padding-right: 10%
  transform: translate(-50%, -50%)

.h1-separator-m
  color: white
  font-size: 22pt
  font-family: 'customfont-sans-regular'
  line-height: 1.2

.footer
  padding: 8% 12%
  font-size: 14pt
  font-family: 'customfont-sans-regular'
  color: $custom-gray-3

.footer-m
  padding: 15% 8%
  font-size: 12pt
  font-family: 'customfont-sans-regular'
  color: $custom-gray-3

.footer-mini-text
  font-size: 7pt
  padding: 0.5em 0

.panel
  color: $custom-gray-4
  position: fixed
  right: 0
  top: 45%
  padding-right: 8%
  font-size: 6pt

.panel-m
  color: $custom-gray-4
  font-size: 6pt

.viewport
  color: $custom-green-main
  font-size: 10pt

.viewport-m
  color: $custom-green-main
  font-size: 6pt

.tools
  padding : 1em 8% 1em 16%

.tools-m
  padding : 0.3em 7%

.question
  color: white
  background-color: $custom-green-main
  padding: 0.5em
  border-radius: 0
  font-size: 3pt

.alert
  color: white
  font-size: 12px
  background-color: $custom-green-2
  line-height: 1.2

@keyframes top_down
    from
        top: 0px
    to
        top: 45%

.anim
  position: fixed
  animation: top_down 1s
  animation-timing-function: linear
</style>
