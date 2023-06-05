<template>
  <div class="form">
    <h1>Formulaire de contact</h1>
    <br /><br />
    <form action="" method="" class="formulaire">
      <div class="nom">
        <label class="txt" for="nom">Nom : </label>
        <br><br>
        <input type="text" id="nom" placeholder="Nom" aria-required="true" />
      </div>
      <div class="prenom">
        <label class="txt" for="prenom">Prenom :</label>
        <br><br>
        <input type="text" id="prenom" placeholder="Prénom" />
      </div>
      <div class="tel">
        <label class="txt" for="tel">Téléphone : </label>
        <br><br>
        <input type="tel" id="tel" placeholder="0609088909" />
      </div>
      <div class="mail">
        <label class="txt" for="email"> Adresse email :</label>
        <br><br>
        <input type="email" id="email" placeholder="exemple@mail.fr" />
      </div>
      <div class="projet">
        <label class="txt" for="choixQ1">Pour quel projet me contactez-vous ?</label>
        <div>
          <input type="radio" id="photo" name="choixQ1"  value="Photo" v-model="selectedProject"/>
          <label for="photo">Photo</label>
        </div>
        <div>
          <input type="radio" id="video" name="choixQ2" value="Video" v-model="selectedProject" />
          <label for="video">Vidéo</label>
        </div>
        <div>
          <input type="radio" id="devWeb" name="choixQ3" value="Developpement web" v-model="selectedProject" />
          <label for="devWeb">Développement web</label>
        </div>
        <div>
          <input type="radio" id="devWeb" name="choixQ4" value="Marketing digital" v-model="selectedProject" />
          <label for="devWeb">Marketing digital</label>
        </div>
      </div>
      <div class="detail" v-if="selectedProject === 'Photo'">
          <label class="txt" for="choixQ1">Quel est votre projet photo ?</label>
          <br><br>
          <select id="choixQ2">
            <option>vehicule</option>
            <option>Immobilier</option>
            <option>Portrait</option>
            <option>clip</option>
          </select>
      </div>
      <div  class="detail" v-if="selectedProject === 'Video'">
          <label class="txt" for="choixQ2">Quel est votre projet video?</label>
          <br><br>
          <select  id="choixQ2">
            <option>Immobiler</option>
            <option>Sport</option>
            <option>Vehicule</option>
          </select>
      </div>
      <div v-if="selectedProject === 'Developpement web'" class="detail">
          <label class="txt" for="choixQ3">Quel est votre projet web ?</label>
          <br><br>
          <select id="choixQ1">
            <option>Site vitrine</option>
            <option>Site e commerce</option>
            <option>Blog</option>
            <option>Autre(precisez dans les commentaires)</option>
          </select>
      </div>
      <div v-if="selectedProject === 'Marketing digital'" class="detail">
          <label class="txt" for="choixQ3">Quel accompagnement souhaitez-vous ?</label>
          <br><br>
          <select id="choixQ1">
            <option>Community management</option>
            <option>Data scientist</option>
            <option>Strategie digital</option>
            <option>UX designer</option>
            <option>Autre(precisez dans les commentaires)</option>
          </select>
      </div>
      <div class="commentaire">
        <label class="txt" for="story">donner moi plus de précision sur le projet</label>
        <br><br>
        <textarea
          id="story"
          name="story"
          minlength="50"
          maxlength="250"
          placeholder="Entrez vos demandes ici"
        ></textarea>
      </div>
      <button class="valider" type="submit">Envoyer</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "Formulaire",
  data(){
    return{
      selectedProject: '',
    }
  },
};
</script>

<style scoped>
h1 {
  font-size: xx-large;
  text-align: center;
  border: 2px solid black;
  border-radius: 10px;
}

.form {
  padding: 5%;
  display: block;
  margin: auto;
  width: 30%;
  max-width: 40%;
  min-width: 40%;
  height: 80%;
  /* box-shadow: 0 15px 25px rgba(0, 0, 0, 0.6); */
  border-radius: 10px;
  background-color: whitesmoke;
  margin-top: 5%;
  margin-bottom: 5%;
}

.txt{
  font-size: x-large;
  text-transform: uppercase
}

.check{
  display: flex;
  flex-direction: row;
}

input{
  background-color: red;
}
.valider{
  background-color: aqua;
}
.valider:hover{
  background-color: red;
}


</style>
