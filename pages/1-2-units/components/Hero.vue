<template>
  <section class="hero">
    <div class="hero-content">
      <h1>Cursos para programadores&nbsp;🚀</h1>
      <p>
        Aprende de profesionales con experiencia en cursos prácticos y sin
        rodeos. Mejora tus habilidades, especialízate, y sigue avanzando en tu
        carrera.
      </p>
      <Btn>Más información</Btn>
    </div>
  </section>
</template>

<style scoped>
.hero {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem 2rem;
  color: #fff;
}
.hero-content {
  max-width: 40ch;
  font-size: 1.5rem;
}
.hero-content h1 {
  font-size: 2.7rem;
}
@media (min-width: 32rem) {
  .hero-content h1 {
    font-size: 3.2rem;
  }
}
.hero-content p {
  margin-bottom: 3rem;
}
</style>

<script>
import Btn from './Btn'

export default {
  components: {
    Btn,
  },
}
</script>
