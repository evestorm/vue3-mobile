<script setup lang="ts">
const route = useRoute()
const router = useRouter()

function onBack() {
  if (window.history.state.back)
    history.back()
  else
    router.replace('/')
}

const { t } = useI18n()

const title = computed(() => {
  if (!route.meta || !route.meta.title)
    return ''
  return route.meta.i18n ? t(route.meta.i18n) : route.meta.title
})

const showLeftArrow = computed(() => {
  return !(!route.meta || route.meta.hideLeftArrow)
})
</script>

<template>
  <VanNavBar
    v-show="title"
    :title="title"
    :fixed="true"
    clickable
    :left-arrow="showLeftArrow"
    @click-left="onBack"
  />
</template>
