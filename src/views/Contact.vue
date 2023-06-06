<template>
  <div class="principale_div">
    <div class="form">
      <div>
        <h1>Formulaire de contact</h1>
        <br /><br />
        <form action="" method="" class="formulaire">
          <div class="nom">
            <input type="text" id="input" placeholder="Entrez votre nom" aria-required="true" />
          </div>
          <br>
          <div class="prenom">
            <input type="text" id="input" placeholder="Entrez votre prenom" aria-required="true" />
          </div>
          <br>
          <div class="tel">
            <input type="tel" id="input" placeholder="Entrez votre numéro" aria-required="true" />
          </div>
          <br>
          <div class="mail">
            <input type="email" id="input" placeholder="Entrez votre mail" aria-required="true" />
          </div>
          <br>
          <div class="projet">
            <label class="txt" for="choixQ1">Pour quel projet me contactez-vous ?</label>

            <div>
              <br>
              <input type="radio" id="checkbox" name="choixQ1" value="Photo" v-model="selectedProject" />
              <label class="police" for="photo">Photo</label>
            </div>
            <div>
              <input type="radio" id="checkbox" name="choixQ2" value="Video" v-model="selectedProject" />
              <label class="police" for="video">Vidéo</label>
            </div>
            <div>
              <input type="radio" id="checkbox" name="choixQ3" value="Developpement web" v-model="selectedProject" />
              <label class="police" for="devWeb">Développement web</label>
            </div>
            <div>
              <input type="radio" id="checkbox" name="choixQ4" value="Marketing digital" v-model="selectedProject" />
              <label class="police" for="devWeb">Marketing digital</label>
            </div>
            <br>
          </div>

          <div class="detail" v-if="selectedProject === 'Photo'">
            <label class="txt" for="choixQ1">Quel est votre projet photo ?</label>
            <br><br>
            <select id="choix">
              <option>vehicule</option>
              <option>Immobilier</option>
              <option>Portrait</option>
              <option>clip</option>
            </select>
          </div>

          <div class="detail" v-if="selectedProject === 'Video'">
            <label class="txt" for="choixQ2">Quel est votre projet video?</label>
            <br><br>
            <select id="choix">
              <option>Immobiler</option>
              <option>Sport</option>
              <option>Vehicule</option>
            </select>
          </div>

          <div v-if="selectedProject === 'Developpement web'" class="detail">
            <label class="txt" for="choixQ3">Quel est votre projet web ?</label>
            <br><br>
            <select id="choix">
              <option>Site vitrine</option>
              <option>Site e commerce</option>
              <option>Blog</option>
              <option>Autre(precisez dans les commentaires)</option>
            </select>
          </div>

          <div v-if="selectedProject === 'Marketing digital'" class="detail">
            <label class="txt" for="choixQ3">Quel accompagnement souhaitez-vous ?</label>
            <br><br>
            <select id="choix">
              <option>Community management</option>
              <option>Data scientist</option>
              <option>Strategie digital</option>
              <option>UX designer</option>
              <option>Autre(precisez dans les commentaires)</option>
            </select>
          </div>
          <br>
          <div class="commentaire">
            <label class="txt" for="story">donnez moi plus de précision sur le projet</label>
            <br><br>
            <textarea id="story" name="story" rows="10" cols="50" minlength="50" maxlength="500"
              placeholder="Entrez vos précisions ici"></textarea>
          </div>
          <br><br>
          <button class="valider" type="submit">Envoyer</button>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Formulaire",
  data() {
    return {
      selectedProject: '',
    }
  },
};
</script>

<style scoped>
h1 {
  font-size: xx-large;
  text-align: center;
  border-top: 1px solid black;
  border-left: none;
  border-right: none;
  border-bottom: 1px solid black;
  padding: 2%;
}


.principale_div {
  margin: 2%;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2rem;
  border: 2px solid black;
  background-color: transparent;
  box-sizing: border-box;
  border-radius: 20px;
}
.form {
  padding: 5%;
  margin: auto;
  width: 50%;
  max-width: 50%;
  min-width: 40%;
  height: 80%;
  box-shadow: 0 15px 25px rgba(0, 0, 0, 0.8);
  border-radius: 20px;
  background-color: rgba(229, 185, 115);
}

.txt {
  font-size: x-large;
  text-transform: uppercase
}


#input {
  border-top: none;
  border-left: none;
  border-right: none;
  border-bottom: 1px solid black;
  width: 90%;
  padding: 5px;
  justify-content: center;
  background-color: rgba(229, 186, 115);
  outline: none;
}

.valider {
  background-color: rgba(229, 186, 115);
}


#choix {
  background-color: rgba(229, 186, 115);
  border-top: none;
  border-left: 1px solid black;
  border-right: none;
  border-bottom: 1px solid black;
  border-bottom-left-radius: 20%;
  outline: none;
}

.police {
  font-size: larger;
}

#story {
  outline: none;
  background-color: rgba(229, 186, 115);
  border-radius: 10px;
  border: 1px solid black;
}


</style>
