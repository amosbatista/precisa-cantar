<template>
  <footer>
    <ul>
      <li>
        Sobre
      </li>
    </ul>
    <p class="rights">
      Criado por <a href="https://amosbatista.com/">Amós Batista</a>. Todos os direitos reservados.
    </p>
  </footer>
</template>

<script>
export default {

}
</script>

<style scoped>
  footer {
    background-color: #301C94;
    display: flex;
    justify-content: flex-start;
    align-items: flex-start;
    align-content: center;
    color: #E0CD41;
    flex-direction: column;
  }
  footer ul li {
    font-size: 90%;
    font-weight: 700;
    list-style: none;
    padding: 0 20px;
    margin: 0px 0 10px;
  }
  footer ul {
    margin-bottom: 0;
  }
  footer .rights {
    padding-left: 20px;
    color: #E0CD41;
    font-size: 50%;
  }
  footer .rights a,
  footer .rights a:visited {
    color: #E0CD41;
  }
</style>
