<script setup>
import { Menu, MenuButton, MenuItems, MenuItem } from "@headlessui/vue";
import { useI18n } from 'vue-i18n'
import i18n from '@/components/i18n.vue'

const { t } = useI18n()
function scrollToTop() {
  window.scrollTo({
    top: 0,
    behavior: 'smooth',
  })
}
</script>

<template>
  <div>
    <!-- Gotop -->
    <div class="fixed right-5 bottom-5 z-50 opacity-30 hover:opacity-100">
      <div class="grid gap-2">
        <div data-tip="切換語言" class="tooltip">
          <i18n />
        </div>
        <div data-tip="回到頂端" class="tooltip tooltip-left">
          <div class="avatar cursor-pointer" @click="scrollToTop">
            <div
              class="mb-8 rounded-full w-12 h-12 md:w-24 md:h-24 ring ring-blue-100 ring-offset-base-100 ring-offset-2"
            >
              <a>
                <img src="@/assets/images/soojin.jpg" />
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Menu -->
    <Menu>
      <div class="navbar shadow-lg bg-neutral text-neutral-content" v-if="$route.meta.title">
        <div class="px-2 mx-2 navbar-start">
          <router-link to="/">
            <div class="w-2/3">
              <img src="@/assets/images/weeekly.png" alt="這是logo" />
            </div>
          </router-link>
        </div>
        <div class="hidden px-2 mx-2 navbar-center lg:flex">
          <div class="flex items-stretch">
            <router-link to="Soojin" class="btn btn-ghost btn-sm rounded-btn">{{ t('name.soojin') }}</router-link>
            <router-link to="Jiyoon" class="btn btn-ghost btn-sm rounded-btn">{{ t('name.jiyoon') }}</router-link>
            <router-link to="Monday" class="btn btn-ghost btn-sm rounded-btn">{{ t('name.monday') }}</router-link>
            <router-link to="Soeun" class="btn btn-ghost btn-sm rounded-btn">{{ t('name.soeun') }}</router-link>
            <router-link to="Jaehee" class="btn btn-ghost btn-sm rounded-btn">{{ t('name.jaehee') }}</router-link>
            <router-link to="Jihan" class="btn btn-ghost btn-sm rounded-btn">{{ t('name.jihan') }}</router-link>
            <router-link to="Zoa" class="btn btn-ghost btn-sm rounded-btn">{{ t('name.zoa') }}</router-link>
          </div>
        </div>
        <div class="navbar-end"></div>
        <div class="flex-none lg:hidden">
          <MenuButton>
            <button class="btn btn-square btn-ghost">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                class="inline-block w-6 h-6 stroke-current"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6h16M4 12h16M4 18h16"
                />
              </svg>
            </button>
          </MenuButton>
        </div>
      </div>
      <MenuItems class="flex-none lg:hidden">
        <MenuItem>
          <div class="flex flex-col">
            <router-link to="Soojin" class="btn btn-ghost btn-sm rounded-btn">{{ t('name.soojin') }}</router-link>
            <router-link to="Jiyoon" class="btn btn-ghost btn-sm rounded-btn">{{ t('name.jiyoon') }}</router-link>
            <router-link to="Monday" class="btn btn-ghost btn-sm rounded-btn">{{ t('name.monday') }}</router-link>
            <router-link to="Soeun" class="btn btn-ghost btn-sm rounded-btn">{{ t('name.soeun') }}</router-link>
            <router-link to="Jaehee" class="btn btn-ghost btn-sm rounded-btn">{{ t('name.jaehee') }}</router-link>
            <router-link to="Jihan" class="btn btn-ghost btn-sm rounded-btn">{{ t('name.jihan') }}</router-link>
            <router-link to="Zoa" class="btn btn-ghost btn-sm rounded-btn">{{ t('name.zoa') }}</router-link>
          </div>
        </MenuItem>
      </MenuItems>
    </Menu>

    <main>
      <router-view />
    </main>
  </div>
</template>
<style lang="scss">
.router-link-exact-active {
  color: #4e5eac;
}
</style>
