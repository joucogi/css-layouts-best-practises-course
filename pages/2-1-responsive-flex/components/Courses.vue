<template>
  <div class="block">
    <section class="courses">
      <h2 class="courses-title">👌 Cursos disponibles</h2>
      <Filters />
      <div class="courses-collection">
        <Card v-for="course in courses" :key="course.title" :course="course" />
      </div>
    </section>
  </div>
</template>

<style scoped>
.block {
  background: #eee;
}

.courses {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 4rem 1rem;
}
.courses-title {
  font-size: 2rem;
}
@media (min-width: 40rem) {
  .courses-collection {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
  }
}
@media (min-width: 60rem) {
  .courses-collection {
    grid-template-columns: 1fr 1fr 1fr;
  }
}
@media (min-width: 70rem) {
  .courses-collection {
    grid-template-columns: 1fr 1fr 1fr 1fr;
  }
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>

<script>
import Card from './Card'
import Filters from './Filters'
import courses from '~/content/courses.json'

export default {
  components: {
    Card,
    Filters,
  },
  data() {
    return {
      courses,
    }
  },
}
</script>
