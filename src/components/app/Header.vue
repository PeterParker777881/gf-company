<template>
  <header class="header">
    <div class="header-top">
      <div class="container">
        <div class="header-top-inner">
          <img class="header-top-logo" src="@/assets/images/header/header-logo.png" />
          <nav class="header-top-nav">
            <ul>
              <li class="header-top-nav-li" v-for="(link, i) in headerTopList" :key="i">
                <router-link class="header-top-nav-link" :to="link.href">{{ link.title }}</router-link>
              </li>
            </ul>
          </nav>
          <Search class="search" />
          <div class="header-top-right">
            <router-link class="header-top-right-link" to="#">
              <img src="@/assets/images/header/cart.svg" />
            </router-link>
            <router-link class="header-top-right-link" to="#">
              <img src="@/assets/images/header/profile.svg" />
              <span>Личный кабинет</span>
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import Search from '@/components/app/Search.vue'
export default {
  components: { Search },
  data: () => ({
    headerTopList: [
      { title: 'Интересности и полезности', href: '#' },
      { title: 'Контакты', href: '#' },
      { title: 'Отзывы', href: '#' },
      { title: 'Доставка и оплата', href: '#' }
    ]
  })
}
</script>

<style lang="scss" scoped>
.header-top {
  background: #f8f8f8;
  padding: 12px 0;
}
.header-top-inner {
  display: flex;
  align-items: center;
}
.header-top-logo {
  display: block;
  width: 100%;
  max-width: 73px;
  height: 60px;
  margin-right: 28px;
}
.header-top-nav {
  margin-right: 123px;
  ul {
    display: flex;
  }
}
.header-top-nav-li {
  margin-right: 24px;
  &:last-child {
    margin-right: 0;
  }
}
.header-top-nav-link {
  line-height: 22px;
  font-weight: 500;
  color: #000;
  text-decoration: none;
}
.search {
  margin-right: 32px;
}
.header-top-right {
  display: flex;
  align-items: center;
}
.header-top-right-link {
  display: flex;
  align-items: center;
  margin-right: 32px;
  text-decoration: none;
  img {
    width: 26px;
    height: 26px;
  }
  span {
    display: block;
    margin-left: 8px;
    line-height: 22px;
    font-weight: 500;
    color: #000;
  }
  &:last-child {
    margin-right: 0;
  }
}
</style>
