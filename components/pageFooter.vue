<template>
  <footer class="container">
    <div class="container-center">
      <ul>
        <li>
          Sobre
        </li>
      </ul>
      <p class="rights">
        Criado por <a href="https://amosbatista.com/">Amós Batista</a>. Todos os direitos reservados.
      </p>
    </div>
  </footer>
</template>

<script>
export default {

}
</script>

<style scoped>
  footer {
    background-color: #301C94;
    color: #E0CD41;
  }
  footer ul li {
    font-size: 90%;
    font-weight: 700;
    list-style: none;
  }
  footer ul {
    margin-bottom: 0;
    padding: 0;
  }
  footer .rights {
    color: #E0CD41;
    font-size: 50%;
  }
  footer .rights a,
  footer .rights a:visited {
    color: #E0CD41;
  }
</style>
