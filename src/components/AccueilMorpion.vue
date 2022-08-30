<template>
  <div class="entete">
    <div class="header">
      <h1>
        <img src="../assets/morpion.png" alt="">
      </h1>
    </div>
  </div>
  <div class="body">
    <div class="corpsreglements">
      <div class="title2">
        <h2>Voici les règles !</h2>
      </div>
      <div class="regles">
        <ul>
          <li>
            <p>Dans un damier de 3/3, chacun votre tour vous aller placer le morpion que vous aurez choisis dans une des
              cases vide restante</p>
          </li>
          <li>
            <p>Le but étant d'aligner votre symbole sur 3 cases que se soit diagonalement, horizontalement ou
              verticalement
            </p>
          </li>
        </ul>
      </div>
      <div class="title3">
        <h3>A vos morpion</h3>
      </div>
      <div class="boutongo">
        <input class="go" type="submit" value="Go !!" @click="jouer">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AccueilMorpion',
  components: {

  },
  methods: {
    jouer() {
      this.$emit('nextStep')
    }
  }
}
</script>


<style scoped>
.entete {
  display: flex;
  width: 100%;
  justify-content: center;

  background-color: #f7edb7;
}

.header {
  display: flex;
  width: 60%;
  background-color: #f3e388;
  justify-content: center;
}

h1 {
  display: flex;
  justify-content: center;
}

h2 {
  display: flex;
  justify-content: center;
  margin: 20px;
  font-size: 45px;
}

h3 {
  display: flex;
  justify-content: center;
  font-size: 32px;
  margin: 25px 0px 15px 0px;
}

img {
  width: 450px;
  height: 240px;
}

.regles {
  display: flex;
  justify-content: center;
  font-size: 17px;
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
}

.boutongo {
  display: flex;
  justify-content: center;
}

.go {
  width: 65px;
  height: 35px;
  font-size: 23px;
  background-color: #99c257;
  border-color: #2E3B1A;
}

.body {
  width: 100%;
  display: flex;
  justify-content: center;
  background-color: #736B40;
}

.corpsreglements {
  width: 80%;
  display: flex;
  flex-direction: column;
  background-color: #D9CA79;
  align-items: center;
}

.title2 {
  background-color: #beb269;
  justify-content: center;
  width: 60%;
}
</style>
