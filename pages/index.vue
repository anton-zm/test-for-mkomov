<template>
  <main class="main">
    <Banner />
    <Action />
    <Title class="section-title" :title="'кто может пользоваться'" />
    <ListSection />
  </main>
</template>

<script>
import Banner from '@/components/banner'
import Action from '@/components/action'
import Title from '@/components/sectionTitle'
import ListSection from '@/components/listsection'
export default {
  components: {
    Banner,
    Action,
    Title,
    ListSection,
  },
}
</script>

<style scoped>
.section-title {
  margin: 48px auto;
}
</style>
