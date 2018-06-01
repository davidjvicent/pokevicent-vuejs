<template lang="pug">
  footer(class='page-footer font-small indigo footer')
    div(class='container')
      div(class='row')
        div(class='col-md-6 py-5 mx-auto')
          div(class='mb-5 flex-center')
            a(class='fb-ic', href='https://www.facebook.com/djassiel26')
              i(class='fa fa-facebook fa-lg white-text PvIcon mr-3 fa-2x')
            a(class='tw-ic', href='https://twitter.com/davidjvicent')
              i(class='fa fa-twitter fa-lg white-text PvIcon mr-3 fa-2x')
            a(class='ins-ic', href='https://www.instagram.com/davidjvicent/')
              i(class='fa fa-instagram fa-lg white-text PvIcon mr-3 fa-2x')
    div(class='footer-copyright py-3 text-center')
      | Hecho con
      span()  💓
      |  por
      strong  David Vicent
</template>

<style>
.footer {
  position: absolute;
  width: 100%;
  background-color: rgb(0, 145, 12)!important;
}

.footer-copyright {
  color: white !important;
}

.PvIcon {
  margin: 25px;
}
</style>
