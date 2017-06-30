<template>
  <div id="app" class="container">
    <div class="header clearfix">
      <nav>
        <ul class="nav nav-pills pull-right">
          <li role="presentation"><router-link :to="{ name: 'home' }" active-class="active">Home</router-link></li>
          <li role="presentation"><router-link :to="{ name: 'about' }" active-class="active">About</router-link></li>
          <li role="presentation"><router-link :to="{ name: 'contact' }" active-class="active">Contact</router-link></li>
        </ul>
      </nav>
      <h3 class="text-muted">Project name</h3>
    </div>

    <router-view></router-view>

    <footer class="footer">
      <p>&copy; 2016 Company, Inc.</p>
    </footer>

  </div> <!-- /container -->
</template>

<script>

  import Vue from 'vue';
  import VueRouter from 'vue-router';

  Vue.use(VueRouter);

  import Home from './Home.vue';
  import About from './About.vue';
  import Contact from './Contact.vue';

  const routes = [
    { path: '/', name: 'home', component: Home },
    { path: '/about', name: 'about', component: About },
    { path: '/contact', name: 'contact', component: Contact }
  ];

  const router = new VueRouter({
    routes
  });

  export default {
    router,
    name: 'app',
    data () {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    }
  }
</script>

<style lang="scss">
#app {
  padding-top: 20px;
  padding-bottom: 20px;
}

/* Everything but the jumbotron gets side spacing for mobile first views */
.header,
.marketing,
.footer {
  padding-right: 15px;
  padding-left: 15px;
}

/* Custom page header */
.header {
  padding-bottom: 20px;
  border-bottom: 1px solid #e5e5e5;
}
/* Make the masthead heading the same height as the navigation */
.header h3 {
  margin-top: 0;
  margin-bottom: 0;
  line-height: 40px;
}

/* Custom page footer */
.footer {
  padding-top: 19px;
  color: #777;
  border-top: 1px solid #e5e5e5;
}

/* Customize container */
@media (min-width: 768px) {
  .container {
    max-width: 730px;
  }
}
.container-narrow > hr {
  margin: 30px 0;
}

/* Main marketing message and sign up button */
.jumbotron {
  text-align: center;
  border-bottom: 1px solid #e5e5e5;
}
.jumbotron .btn {
  padding: 14px 24px;
  font-size: 21px;
}

/* Supporting marketing content */
.marketing {
  margin: 40px 0;
}
.marketing p + h4 {
  margin-top: 28px;
}

/* Responsive: Portrait tablets and up */
@media screen and (min-width: 768px) {
  /* Remove the padding we set earlier */
  .header,
  .marketing,
  .footer {
    padding-right: 0;
    padding-left: 0;
  }
  /* Space out the masthead */
  .header {
    margin-bottom: 30px;
  }
  /* Remove the bottom border on the jumbotron for visual effect */
  .jumbotron {
    border-bottom: 0;
  }
}
</style>
