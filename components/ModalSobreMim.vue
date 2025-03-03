<template>
    <div v-if="mostrar" class="modal-overlay">
        <div class="modal-content">
        <h2>Sobre mim</h2>
        <p>Olá meu nome é Felipe Pereira, sou <strong>Analista/Desenvolvedor desde 2009</strong>, com mais de 10 anos de experiência no desenvolvimento de sistemas. Minha missão é criar soluções tecnológicas eficientes e seguras, alinhadas às necessidades do negócio e dos clientes.</p>

        <p>Atualmente, faço parte de uma <strong>equipe de desenvolvimento focada em soluções para o mercado financeiro</strong>, trabalhando em projetos que envolvem <strong>modernização de sistemas e transformação digital</strong>.</p>

        <p>Tenho experiência com <strong>o ecossistema .NET, T-SQL, JavaScript, Windows Forms, HTTP, HTML e programação orientada a objetos</strong>. Além disso, atuo em projetos estruturados em <strong>Java 17, Python, DynamoDB, Amazon RDS e DB2</strong>, ampliando minha atuação no desenvolvimento de sistemas escaláveis e distribuídos.</p>

        <p>Minha atuação envolve <strong>participação nos processos de discovery e delivery</strong>, colaborando no <strong>refinamento de novas features</strong> para garantir que estejam alinhadas às necessidades do negócio e dos usuários. Também sou responsável pelo <strong>desenvolvimento de novas funcionalidades, correção de bugs e otimização de performance</strong>. Além disso, colaboro ativamente com analistas, desenvolvedores, testers e stakeholders para garantir que as soluções entregues sejam eficientes e escaláveis.</p>

        <div class="modal-footer">
            <button @click="fecharModal" 
                class="px-4 py-2 bg-gray-200 text-gray-700 rounded hover:bg-gray-300 transition">
                Fechar
            </button>
        </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        mostrar: Boolean
    },
    emits: ["fechar"], // Define que esse componente emite um evento chamado "fechar"
    methods: {
        fecharModal() {
        this.$emit("fechar"); // Emite o evento "fechar" para o index.vue
        }
    }
};
</script>
<style scoped>
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px; /* Garante espaçamento em telas menores */
}


.modal-content {
  background: white;
  padding: 20px;
  border-radius: 8px;
  max-width: 700px; /* Aumenta a largura do modal */
  width: 90%; /* Responsivo para telas menores */
  max-height: 75vh; /* Reduz a altura máxima do modal */
  overflow-y: auto; /* Adiciona rolagem vertical se necessário */
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
}

.modal-content p {
  margin-bottom: 16px; /* Espaçamento entre parágrafos */
  text-align: left; /* Alinha o texto à esquerda */
}

.modal-footer {
  display: flex;
  justify-content: flex-end; /* Alinha o botão à direita */
  margin-top: 20px; /* Dá um espaçamento superior */
}

.modal-content h2 {
  font-size: 1.5rem; /* Aumenta o tamanho da fonte */
  font-weight: bold; /* Deixa o título em negrito */
  text-align: center; /* Centraliza o título */
  margin-bottom: 16px; /* Adiciona um espaçamento abaixo do título */
  color: #333; /* Usa uma cor escura para mais contraste */
}
</style>
