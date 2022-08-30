<template>
    <div class="header">
        <h1>Choisis ton morpion</h1> <br>
    </div>
    <div class="choixmorpion">
        <div class="morpion">Croix <input type="checkbox" v-model="choixFaitCroix" checked></div>
        <div class="arrow"><img scr="../assets/fleche_droite.png" alt=""></div>
        <div class="morpion">Rond <input type="checkbox" v-model="choixFaitRond" checked></div>
    </div>
    <div class="boutonpartie">
        <input class="cestpartie" type="submit" value="C'est partie" @click="jouer">
    </div>
</template>

<script>
export default {
    name: 'ChoixMorpion',
    data() {
        return {
            choixFaitCroix: false,
            choixFaitRond: false,
        }
    },
    components: {

    },
    methods: {
        jouer() {
            this.$emit('nextStep')
        },
    }
}
</script>


<style scoped>
.header {
    display: flex;
    width: 100%;
    background-color: bisque;
    justify-content: center;
}

h1 {
    display: flex;
    justify-content: center;
}

.choixmorpion {
    width: 100%;
    height: 300px;
    display: flex;
    justify-content: center;
}

.morpion {
    width: 35%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.arrow {
    width: 30%;
    display: flex;
    justify-content: center;
    align-items: center;
}

img {
    width: 220px;
    height: 200px;
}

.boutonpartie {
    width: 100%;
    display: flex;
    justify-content: center;
}


.cestpartie {
    justify-content: center;
    padding: 15px 80px;
    margin: 10px 4px;
    color: rgb(197, 117, 13);
    font-family: sans-serif;
    text-transform: uppercase;
    text-align: center;
    position: relative;
    text-decoration: none;
    display: inline-block;
    border: 1px solid;
    border-radius: 9px;
}

.cestpartie::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    display: block;
    width: 100%;
    height: 100%;
    z-index: -1;
    -webkit-transform: scaleY(0.1);
    transform: scaleY(0.1);
    transition: all 0.4s;
    border-radius: 50% 20% / 10% 40%;
}

.cestpartie:hover {
    color: #b414badc;
}

.cestpartie:hover::before {
    opacity: 1;
    background-color: #f7c2f9;
    -webkit-transform: scaleY(1);
    transform: scaleY(1);
    transition: -webkit-transform 0.6s cubic-bezier(0.08, 0.35, 0.13, 1.02), opacity 0.4s;
    transition: transform 0.6s cubic-bezier(0.08, 0.35, 0.13, 1.02), opacity;
}
</style>