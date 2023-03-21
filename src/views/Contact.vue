<template>
   <div class="form">
    <h1>Formulaire de contact</h1>
    <hr><br>
    <form action="" method="" class="formulaire">
      <div class="nom">
        <label for="nom">Nom : </label>
        <input type="text" id="nom" placeholder="Nom" aria-required="true">
      </div>
      <div class="prenom">
        <label for="prenom">Prenom :</label>
        <input type="text" id="prenom" placeholder="Prénom">
      </div>
      <div class="tel">
        <label for="tel">Téléphone : </label>
        <input type="tel" id="tel" placeholder="0609088909">
      </div>
      <div class="mail">
        <label for="email"> Adresse email :</label>
        <input type="email" id="email" placeholder="exemple@mail.fr">
      </div>
      <div class="projet">
        <label for="choixQ1">Pour quel projet me contactez-vous ?</label>
        <div>
          <input type="radio" id="devWeb" name="choixQ1" value="developpement web">
          <label for="devWeb">Développement web</label>
        </div>
        <div>
          <input type="radio" id="photo" name="choixQ1" value="photo">
          <label for="photo">Photo</label>
        </div>
        <div>
          <input type="radio" id="video" name="choixQ1" value="video">
          <label for="video">Vidéo</label>
        </div>
      </div>
    <div class="detail">
      <div class="detail1">
        <label for="choixQ2">Quel est votre projet web ?</label>
        <select id="choixQ2">
          <option>Site vitrine</option>
          <option>Site e commerce</option>
          <option>Blog</option>
          <option>Autre(precisez dans les commentaires)</option>
        </select>
      </div>
      <div class="detail2">
        <label for="choixQ2">Quel est votre projet photo ?</label>
        <select id="choixQ2">
          <option>vehicule</option>
          <option>Immobilier</option>
          <option>Portrait</option>
          <option>clip</option>
        </select>
      </div>
      <div class="detail3">
        <label for="choixQ2">Quel est votre projet video?</label>
        <select id="choixQ2">
          <option>Immobiler</option>
          <option>Sport</option>
          <option>Vehicule</option>
        </select>
      </div>
    </div>
      <div class="commentaire">
        <label for="story">donner moi plus de précision sur le projet</label>
        <textarea id="story" name="story" minlength="50" maxlength="250" placeholder="Entrez vos demandes ici"></textarea>
      </div>
      <button class="valider" type="submit">Envoyer</button>

    </form>
   </div>
    
</template>

<script>

  export default {
  data() {
    return {
      nom : '',
      prenom : ''
    }
  }
}
 
</script>

<style scoped>

.form{
  display: block;
    margin:auto;
    width: 30%;
    max-width: 60%;
    min-width: 60%;
    height: 80%;
    box-shadow: 0 15px 25px rgba(0,0,0,.6);
    border-radius: 10px;
}

.nom{
  border: solid 2px #120A19;
}
.prenom{
  border: solid 2px #120A19;
}
.tel{
  border: solid 2px #120A19;
}
.mail{
  border: solid 2px #120A19;
}
.projet{
  border: solid 2px #120A19;
}

.detail{
  border: solid 2px #120A19;
}

.commentaire{
  border: solid 2px #120A19;
}

.valider{
  border: solid 2px #120A19;
}


</style>

