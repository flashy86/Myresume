<template>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cookie&family=Overlock:ital@0;1&display=swap" rel="stylesheet">

  <div class="home">

    <div id="titre" class="titre">
      <h1>Anne-Charlotte LUCAS</h1>
      <h2>Conceptrice et Développeuse<br> d'Applications</h2>
      <h3>Nouvelle développeuse curieuse en reconversion professionnelle</h3>
    </div>

      <img class="photo" alt="Anne-Charlotte LUCAS" src="../assets/photo_Id.png">

      <aside class="competences">
          <h4>Compétences</h4><br>
    <CompetencesItem
    v-for="item in data_competences"
                     :key = "item.libelle"
                     :libelle = "item.libelle"
                     :score = "item.score"
                     :description = "item.description"
    />
      </aside>

    <section class="diplome">
        <h4>Diplômes et Formations</h4><br>
        <DiplomeItem
                     v-for="item in datas_item"
                     :key = "item.name"
                     :name = "item.name"
                     :ecole = "item.ecole"
                     :site = "item.site"
                     :date_debut = "item.date_debut"
                     :date_fin = "item.date_fin"
                     :presentation = "item.presentation"
        />
    </section>
    <section class="experiences">
        <h4>Expériences Professionnelles</h4>
        <ExperiencesProItem
            v-for="item in datas_exp"
            :key = "item.poste"
            :poste = "item.poste"
            :entreprise = "item.entreprise"
            :localisation = "item.localisation"
            :datedeb = "item.datedeb"
            :datefin = "item.datefin"
            :description = "item.description"
        />
    </section>
    <aside class="infos">
        <InfosItem/>
    </aside>

      <aside class="langue">
          <h4>Langues</h4>
          <LangueItem ></LangueItem>
      </aside>
      <aside class="hobbies">
        <h4>Hobbies</h4>
          <HobbiesItem/>
      </aside>

      <section class="projets">
            <h4>Projets Informatique</h4>
          <ProjetsItem
            v-for="item in datas_projets"
                :key="item.name "
                :name = "item.name"
                :description = "item.description"
                :date = "item.date"
                :technologies = "item.technologies"/>
      </section>

    <Logos>
        //section à faire
    </Logos>
  </div>
</template>

<script>
//----------IMPORT DES COMPOSANTS------------------------
import CompetencesItem from "../components/CompetencesItem";
import DiplomeItem from "../components/DiplomeItem";
import ExperiencesProItem from "../components/ExperiencesProItem";
import HobbiesItem from "../components/HobbiesItem";
import InfosItem from "../components/InfosItem";
import LangueItem from "../components/LangueItem";
import ProjetsItem from "../components/ProjetsItem";
import Logos from "../components/Logos";



export default {
  name: 'Home',

  // -------------- DEFINITION DES COMPOSANTS------------
  components: {
    Logos,
    CompetencesItem,
    DiplomeItem,
    ExperiencesProItem,
    HobbiesItem,
    InfosItem,
    LangueItem,
    ProjetsItem
  },
  //------------------------DATAS-------------------------
  data: function () {
    return {
      datas_item: [
        {
          name: "Titre Conceptrice Développeuse Informatique",
          ecole: 'E.N.I. à distance',
          site: 'https://www.eni-ecole.fr/ecole/campus-en-ligne/',
          date_deb: '29/03/2021',
          date_fin: '15/01/2022',
          presentation: "String1"
        },
        {
          name: 'Master 2 Management des Systèmes d\'Informations et de Communications',
          ecole: 'I.A.E Brest',
          site: 'https://www.univ-brest.fr/iae',
          date_debut: '01/09/2014',
          date_fin: '15/11/2015',
          presentation: "String2"
        },
        {
          name: 'Master 1 Sciences du Management parcours Finance Comptabilité',
          ecole: 'I.A.E Brest',
          site: 'https://www.univ-brest.fr/iae',
          date_debut: '01/09/2011',
          date_fin: '30/06/2012',
          presentation: "string 3"
        },
        {
          name: 'Licence Economie - Gestion',
          ecole: 'Universite de Bretagne Occidentale',
          site: 'https://www.univ-brest.fr/',
          date_debut: '01/09/2008',
          date_fin: '30/06/2011',
          presentation: "string 4"
        }
      ],
      data_competences: [
        {
          libelle: 'Interface utilisateur dynamique',
          description: '    Html5, CSS, Javascript, Twig, divers\n' +
              '    frameworks et/ou pluggins comme\n' +
              '    Bootstrap 4',
          score: '83'
        },
        {
          libelle: ' Programmation logicielle',
          description: 'Langages abordés en back-end: Java,' +
              'Java SE, Java EE, PHP, Php&Symfony',
          score: '60'
        },
        {
          libelle: 'Programmation front-end',
          description: 'HTML5, CSS3, Js, Ts, Twig',
          score: '70'
        },
        {
          libelle: 'Base de Données',
          description: 'Création de la base de donnée, Analyse et Manipulation des données',
          score: '67'
        }
      ],

      datas_exp:[
          {
              poste: 'Assistante aux affaires projet terre',
              entreprise:'CIRISI' ,
              localisation: 'Brest',
              datedeb: '02/2020',
              datefin: '04/2020',
              description:'description à remplir'
          },
          {
              poste: 'Assistante aux affaires projet terre',
              entreprise:'CIRISI' ,
              localisation: 'Brest',
              datedeb: '11/2019',
              datefin: '12/2019',
              description:'description à remplir'
          },
          {
              poste: 'Comptable',
              entreprise:'GENAVIR' ,
              localisation: 'Plouzané',
              datedeb: '03/2018',
              datefin: '06/2018',
              description:'description à remplir'
          },
          {
              poste: 'Collaboratrice comptable',
              entreprise:'CEDEM' ,
              localisation: 'Brest',
              datedeb: '10/2017',
              datefin: '12/2017',
              description:'description à remplir'
          },
          {
              poste: 'Collaboratrice comptable',
              entreprise:'CELLERIER, BENEAT & ASSOCIES' ,
              localisation: 'Brest',
              datedeb: '08/2016',
              datefin: '06/2017',
              description:'description à remplir'
          },
          {
              poste: 'Contrôleuse de Gestion',
              entreprise:'PWC' ,
              localisation: 'Neuilly-sur-Seine',
              datedeb: '01/2016',
              datefin: '08/2016',
              description:'description à remplir'
          }
      ],
      datas_projets:[
          {
              name:'Projet BDE',
              date: '08-2021',
              description: 'ecole',
              technologies: 'string a completer'
          },
          {
              name: 'Projet Enchères',
              date: '06-2021',
              description: 'ecole',
              technologies: 'string a completer'
      },
      {
              name: 'Création d\'une bucket-list Symfony',
              date: '07-2021',
              description: '',
              technologies: 'string a completer'
      },
      {
              name: 'Création d\'un mini site e-commerce Symfony & MySQL',
              date: '07-2021',
              description: '',
              technologies: 'string a completer'
      },
      {
              name: 'Création d\'un site e-commerce Wordpress',
              date: '09-2021',
              description: '',
              technologies: 'string a completer'
      },
      ]
    }
  }
}
</script>
<style lang="scss">
$color1: #333033B8;
$color2: #EE3191EF;
$color3: #f8e9f8;
$color_titre: #888188;

* {
  margin: 0;
  padding: 0;
}
.home{
  display: grid;
  grid-template:  "titre photo" auto
                  "diplome infos" auto
                  "projets competences" auto
                  "experiences competences " auto
                  "logo langue" auto
                  "logo hobbies" auto
                  /0.66fr 0.33fr;
  background-color: $color1;
  h1{
    font-size: 7em;
  }
  h2{
    font-size: 4em;
    color: $color_titre;
  }
  h3{
    font-size: 2em;
  }
  h4{
    font-size: 1.5em;
    color: $color2;


  }
  #titre{
    padding: 2em;
    background-color: $color1;
    color: $color3;


  }


}
.photo{

 justify-self: center;
  align-self: center;
  height: 15em;
}
.diplome{
  grid-area: diplome;
  background-color: $color3;
}
.infos{
  grid-area: infos;
  background-color: $color1;
  color: $color3;
}
.experiences{
  grid-area: experiences;
  background-color: $color3;
}
.competences{
  grid-area: competences;
  background-color: $color1;
  color: $color3;
}
.langue{
  grid-area: langue;
  background-color: $color1;
  color: $color3;
}
.hobbies{
  grid-area: hobbies;
  background-color: $color1;
  color: $color3;
}
.projets{
  background-color: $color3;
}


</style>
