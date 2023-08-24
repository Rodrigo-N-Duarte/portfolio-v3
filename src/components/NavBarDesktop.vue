<template>
  <v-sheet class="dark-texture-background desktop-div">
    <v-row class="py-5">
      <v-col cols="1"></v-col>
      <v-col align="start" cols="9">
        <router-link class="name-link mx-5" to="/">Rodrigo Duarte</router-link>
        <router-link v-for="item in desktopItens" :key="item" :to="item.link"
                     class="default-link mx-2 text-uppercase">{{ item.name }}
        </router-link>
      </v-col>
      <v-col cols="1"></v-col>
    </v-row>
  </v-sheet>
  <v-sheet class="mobile-app-bar" justify="center">
    <v-row>
      <v-bottom-navigation class="dark-texture-background text-white">
        <v-row justify="space-around">
          <v-col v-for="item in mobileItens" :key="item" :value="item.name" class="d-flex align-center justify-center"
                 cols="2">
            <v-btn>
              <router-link
                  :to="item.link"
                  class="text-uppercase text-white text-decoration-none d-flex flex-column justify-center align-center">
                <v-icon>{{ item.icon }}</v-icon>
                <span>{{ item.name }}</span>
              </router-link>
            </v-btn>
          </v-col>
        </v-row>
      </v-bottom-navigation>
    </v-row>
  </v-sheet>
</template>

<script>

export default {
  name: 'NavBarDesktop',
  data() {
    return {
      desktopItens: [
        {
          name: 'Home',
          link: '/'
        },
        {
          name: 'About',
          link: '/about'
        },
        {
          name: 'Projects',
          link: '/projects'
        },
        {
          name: 'Skills',
          link: '/skills'
        },
        {
          name: 'Experience',
          link: '/experience'
        },
        {
          name: 'Contact',
          link: '/contact'
        }
      ],
      mobileItens: [
        {
          name: '',
          link: '/',
          icon: 'mdi-home'
        },
        {
          name: '',
          link: '/projects',
          icon: 'mdi-chart-arc'
        },
        {
          name: '',
          link: '/skills',
          icon: 'mdi-book'
        },
        {
          name: '',
          link: '/experience',
          icon: 'mdi-compass'
        },
        {
          name: '',
          link: '/contact',
          icon: 'mdi-phone'
        }
      ]
    }
  },
}
</script>

<style>
.default-link {
  font-family: 'Inter', sans-serif;
  font-size: 15px;
  color: aliceblue;
  text-decoration: none;
  position: relative;
  overflow: hidden;
  padding: 5px;
}

.default-link::after {
  content: '';
  display: block;
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 1px;
  background-color: white;
}

.default-link:hover::after {
  animation: loading-bar 0.15s linear forwards;
}

@keyframes loading-bar {
  0% {
    width: 0;
  }
  100% {
    width: 100%;
  }
}


.name-link {
  color: aliceblue;
  text-decoration: none;
  font-family: 'Inter', sans-serif;
}

.desktop-div {
  display: block;
}

.mobile-app-bar {
  display: none;
}

@media (max-width: 1279px) {
  .desktop-div {
    display: none;
  }

  .mobile-app-bar {
    display: block;
  }
}

@media (min-width: 1280px) {
  .mobile-app-bar {
    display: none;
  }

  .desktop-div {
    display: block;
  }
}

.menu-mobile {
  background-color: aliceblue;
  padding: 20px 80px 20px 20px;
}
</style>
