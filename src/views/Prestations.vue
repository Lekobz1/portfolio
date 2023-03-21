<template>
    <div class="specialties">
      <div class="specialty" v-for="(specialty, index) in specialities" :key="index">
            <h1> {{ specialty.title }} </h1>
            <button @click="toggleSpecialty(index)">{{ specialty.isOpen ? 'Fermer cette prestation' : 'Afficher la prestations' }}</button>
        <div v-if="specialty.isOpen">
            <p>{{ specialty.text }}</p>
        </div>
      </div>
    </div>
</template>
    
  
  <script>
  export default {
    data() {
      return {

        specialities: [
          { title: "Developpement web", text: "Bienvenue sur mon portfolio ! Je suis un développeur passionné et expérimenté dans les domaines du frontend et du backend. Ma spécialité est de travailler avec les langages informatiques HTML, CSS, JavaScript et le framework Vue.js pour le développement de sites web réactifs et dynamiques. Je suis également un expert en PHP et je travaille avec les frameworks Symfony et Laravel pour le backend. Je suis également compétent dans l'utilisation des outils de conception tels qu'Adobe XD et Figma pour la création de maquettes de sites web. J'aime travailler en étroite collaboration avec mes clients pour comprendre leurs besoins et leurs objectifs. Je peux également rédiger des cahiers des charges pour assurer que tous les aspects du projet sont pris en compte. Je suis fier de fournir des prestations de haute qualité qui répondent aux attentes de mes clients. Mon approche est centrée sur le client et j'accorde une grande importance à la communication et à la collaboration tout au long du processus de développement. Je suis convaincu que mon expérience et mes compétences me permettent de proposer des solutions créatives et innovantes pour répondre aux besoins de chaque projet. N'hésitez pas à me contacter pour discuter de vos projets de développement web. Je suis impatient de travailler avec vous pour créer des sites web uniques et exceptionnels qui répondent à vos besoins spécifiques.", isOpen: false },
          { title: "Photographie", text: "Bienvenue sur mon site de photographie ! Je suis un photographe passionné et expérimenté, spécialisé dans la street photo, le portrait, les concerts et les voitures. J'utilise un Canon EOS 90D pour capturer des images exceptionnelles qui racontent des histoires uniques et inoubliables.Je suis également compétent dans l'utilisation de logiciels de retouche d'images tels que Photoshop et Lightroom pour créer des images qui correspondent exactement à vos besoins et à vos attentes. J'aime travailler en étroite collaboration avec mes clients pour comprendre leurs besoins et leur vision, afin de créer des images qui reflètent leur personnalité et leur style.Je suis fier de fournir des prestations de haute qualité qui répondent aux attentes de mes clients. Mon approche est centrée sur le client et j'accorde une grande importance à la communication et à la collaboration tout au long du processus de prise de vue et de post-production. Je suis convaincu que mon expérience et mes compétences me permettent de proposer des solutions créatives et innovantes pour répondre aux besoins de chaque projet.N'hésitez pas à me contacter pour discuter de vos projets de photographie. Je suis impatient de travailler avec vous pour créer des images qui racontent votre histoire de manière unique et inoubliable.", isOpen: false },
          { title: "Video", text: "Bienvenue sur mon site de production vidéo ! Je suis un vidéaste passionné et expérimenté, spécialisé dans la réalisation de clips, de vidéos de vente immobilière, de street vidéos, de paysages et de sports en tout genre. J'utilise un Canon EOS 90D et un drone DJI Mini Pro 3 pour capturer des images exceptionnelles qui racontent des histoires uniques et inoubliables.Je suis compétent dans l'utilisation de ces équipements pour capturer des images incroyables qui correspondent exactement à vos besoins et à vos attentes. Je suis attentif à chaque détail, en m'assurant que chaque prise de vue soit réalisée avec soin et professionnalisme.Je suis fier de fournir des prestations de haute qualité qui répondent aux attentes de mes clients. Mon approche est centrée sur le client et j'accorde une grande importance à la communication et à la collaboration tout au long du processus de réalisation de la vidéo. Je suis convaincu que mon expérience et mes compétences me permettent de proposer des solutions créatives et innovantes pour répondre aux besoins de chaque projet.N'hésitez pas à me contacter pour discuter de vos projets vidéo. Je suis impatient de travailler avec vous pour créer des vidéos uniques et mémorables qui racontent votre histoire de manière inoubliable.", isOpen: false },
        ],
      };
    },
    methods: {
      toggleSpecialty(index) {
        this.specialities[index].isOpen = !this.specialities[index].isOpen;
      },
    },
  };
  </script>

<style>


.specialties {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
   
}

.specialty {
  width: 50%;
  margin: 1rem;
  padding: 1rem;
  border: 1px solid black;
}

.specialty h1 {
  margin-top: 0;
  color: crimson;
}

.specialty img {
  width: 100%;
  max-height: 200px;
  object-fit: cover;
}

.specialty button {
  margin-top: 1rem;
  color: crimson;
}

.specialty p {
  margin: 1rem 0;
  font-size: 1rem;
  line-height: 1.5;
  color: darkorange;
}

</style>

  

  