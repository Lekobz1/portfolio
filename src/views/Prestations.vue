<template>
  <div class="specialties">
    <div class="specialty" v-for="(specialty, index) in specialities" :key="index">
      <h1> {{ specialty.title }} </h1>
      <button  @click="toggleSpecialty(index)">{{ specialty.isOpen ? 'Fermer cette prestation' : 'Afficher la prestations' }}</button>
      <div v-if="specialty.isOpen">
        <img src="../assets/bateau.jpg" alt="bateau">
        <img src="../assets/devcar.jpg" alt="devcar">
        <img src="../assets/photocar.jpg" alt="devcar">
        <img src="../assets/videocar.jpg" alt="devcar">
        <p>{{ specialty.text }}</p>
        
        <div v-if="specialty.showContact">
          <a href="/contact">Contactez-moi</a>
        </div>
        <div v-if="specialty.showPortfolio">
          <a href="/portfolio">Visiter le portfolio</a>
        </div>
      </div>
    </div>
  </div>
</template>
  
<script>
export default {
  data() {
    return {
      specialities: [
        {
          title: "développement web",
          text: "Tu veux un site pour vendre des chevres naine ?",
          showContact: false,
          showPortfolio: false,
        },
        {
          title: "Photographie",
          text: " viens faire des photos de tes plus beau paté de campagne",
          showContact: false,
          showPortfolio: false,
        },
        {
          title: "Video et film",
          text: "No porn only drone",
          showContact: false,
          showPortfolio: false,
        },
        {
          title: "Marketing Digital",
          text: "viens je t'aide à vendre. Spécialiste thug",
          showContact: false,
          showPortfolio: false,
        },
      ],
    };
  },
  methods: {
    toggleSpecialty(index) {
      this.specialities.forEach((specialty, i) => {
        if (i === index) {
          specialty.isOpen = !specialty.isOpen;
          specialty.showContact = true; // ajouter la carte pour le contact
          specialty.showPortfolio = true; // ajouter la carte pour le portfolio
        } else {
          specialty.isOpen = false;
          specialty.showContact = false;
          specialty.showPortfolio = false;
        }
      });
    },
  },
};
</script>

<style scoped>
.specialties {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;


}

.specialty {
  width: 50%;
  margin: 1rem;
  padding: 1rem;
  border: 3px solid black;
  border-radius: 10%;
  background-color: rgba(249, 244, 237, 1);
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

h1{
  font-size: xx-large;
  text-align: center;
}

button{
  border: 0;
  background: transparent;
  color: black;
  position: relative;
}

.card {
  display: inline-block;
  width: 200px;
  height: 200px;
  border: 1px solid #ccc;
  margin: 10px;
  padding: 10px;
}

.card img {
  width: 100%;
  height: 70%;
  object-fit: cover;
  margin-bottom: 10px;
}

.card h3 {
  font-size: 16px;
  margin-bottom: 10px;
}

.card p {
  font-size: 14px;
  margin-bottom: 10px;
}

.card button {
  display: block;
  width: 100%;
  margin-top: auto;
  background-color: #0077cc;
  color: #fff;
  border: none;
  padding: 10px;
  cursor: pointer;
  transition: background-color 0.3s ease-in-out;
}

.card button:hover {
  background-color: #005ea0;
}

.card.contact img {
  content: url(path/to/contact-image.jpg);
}

.card.portfolio img {
  content: url(path/to/portfolio-image.jpg);
}


</style>

{ title: "Developpement web", text: "Bienvenue sur mon portfolio ! Je suis un développeur passionné et expérimenté dans les domaines du frontend et du backend. Ma spécialité est de travailler avec les langages informatiques HTML, CSS, JavaScript et le framework Vue.js pour le développement de sites web réactifs et dynamiques. Je suis également un expert en PHP et je travaille avec les frameworks Symfony et Laravel pour le backend. Je suis également compétent dans l'utilisation des outils de conception tels qu'Adobe XD et Figma pour la création de maquettes de sites web. J'aime travailler en étroite collaboration avec mes clients pour comprendre leurs besoins et leurs objectifs. Je peux également rédiger des cahiers des charges pour assurer que tous les aspects du projet sont pris en compte. Je suis fier de fournir des prestations de haute qualité qui répondent aux attentes de mes clients. Mon approche est centrée sur le client et j'accorde une grande importance à la communication et à la collaboration tout au long du processus de développement. Je suis convaincu que mon expérience et mes compétences me permettent de proposer des solutions créatives et innovantes pour répondre aux besoins de chaque projet. N'hésitez pas à me contacter pour discuter de vos projets de développement web. Je suis impatient de travailler avec vous pour créer des sites web uniques et exceptionnels qui répondent à vos besoins spécifiques." },
        { title: "Photographie", text: "Bienvenue sur mon site de photographie ! Je suis un photographe passionné et expérimenté, spécialisé dans la street photo, le portrait, les concerts et les voitures. J'utilise un Canon EOS 90D pour capturer des images exceptionnelles qui racontent des histoires uniques et inoubliables.Je suis également compétent dans l'utilisation de logiciels de retouche d'images tels que Photoshop et Lightroom pour créer des images qui correspondent exactement à vos besoins et à vos attentes. J'aime travailler en étroite collaboration avec mes clients pour comprendre leurs besoins et leur vision, afin de créer des images qui reflètent leur personnalité et leur style.Je suis fier de fournir des prestations de haute qualité qui répondent aux attentes de mes clients. Mon approche est centrée sur le client et j'accorde une grande importance à la communication et à la collaboration tout au long du processus de prise de vue et de post-production. Je suis convaincu que mon expérience et mes compétences me permettent de proposer des solutions créatives et innovantes pour répondre aux besoins de chaque projet.N'hésitez pas à me contacter pour discuter de vos projets de photographie. Je suis impatient de travailler avec vous pour créer des images qui racontent votre histoire de manière unique et inoubliable." },
        { title: "Video", text: "Bienvenue sur mon site de production vidéo ! Je suis un vidéaste passionné et expérimenté, spécialisé dans la réalisation de clips, de vidéos de vente immobilière, de street vidéos, de paysages et de sports en tout genre. J'utilise un Canon EOS 90D et un drone DJI Mini Pro 3 pour capturer des images exceptionnelles qui racontent des histoires uniques et inoubliables.Je suis compétent dans l'utilisation de ces équipements pour capturer des images incroyables qui correspondent exactement à vos besoins et à vos attentes. Je suis attentif à chaque détail, en m'assurant que chaque prise de vue soit réalisée avec soin et professionnalisme.Je suis fier de fournir des prestations de haute qualité qui répondent aux attentes de mes clients. Mon approche est centrée sur le client et j'accorde une grande importance à la communication et à la collaboration tout au long du processus de réalisation de la vidéo. Je suis convaincu que mon expérience et mes compétences me permettent de proposer des solutions créatives et innovantes pour répondre aux besoins de chaque projet.N'hésitez pas à me contacter pour discuter de vos projets vidéo. Je suis impatient de travailler avec vous pour créer des vidéos uniques et mémorables qui racontent votre histoire de manière inoubliable."},

  