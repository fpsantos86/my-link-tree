<template>
    <div>
      <ProfileInfo 
        photo ="https://placehold.co/400x400"
        title="Felipe Pereira"  
        subtitle ="@felipepereira" 
        headline="Technology | Product "/>
        <main class="max-w-xs mx-auto">
          <ButtonAction link="https://www.linkedin.com/in/felipe-pereira-06962a31/" text="Linkedin" icon="🔗" />
          <ButtonAction link="https://wa.me/+5527996605069/" text="Whatsapp" icon="💬" />
          <ButtonAction link="https://github.com/fpsantos86" text="Github" icon="👨🏻‍💻" />
          <ButtonAction link="https://www.instagram.com/felipesantos5557" text="Instagram" icon="🤳" />
          <!-- Botão "Sobre mim" reutilizando o componente -->
          <ButtonAction text="Sobre mim" icon="🙋🏻‍♂️" @click="abrirModal" />
        </main>
     <!-- Modal -->
     <ModalSobreMim :mostrar="modalAberto" @fechar="modalAberto = false" />
    </div>
</template>


<script>
import ModalSobreMim from "@/components/ModalSobreMim.vue";

export default {
  components: {
    ModalSobreMim,
  },
  data() {
    return {
      modalAberto: false,
    };
  },
  methods: {
    abrirModal() {
      this.modalAberto = true;
    },
  },
};
</script>