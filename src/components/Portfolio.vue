<template>
    <div>
        <div class="compagny" v-for="compagny in compagnies" :key="compagny.id">
            <div class="row compagny-title">
                <h1 class="compagny-label">{{compagny.label}}</h1>
                <img v-if="compagny.img != null" :src="compagny.img" :width="compagny.imgWidth"/>
            </div>
            <br>
            <div class="porfolio">

                <div class="realisation" v-for="realisation in compagny.realisations" :key="realisation.id">
                    <Realisation class="resalisation-body" :realisation="realisation"/>
                </div>
            </div>
        </div>
        
    </div>
</template>

<script>
import Realisation from "./Realisation"
import SpectrumImg from "@/assets/spectrum.png"
import AutoCompletionImg from "@/assets/autocomplete.png"
import HandsontableImg from "@/assets/handsontable.png"
import GanacosImg from "@/assets/logo_ganacos.png"
import ProgidysImg from "@/assets/logo_progidys.png"
import ETIBImg from "@/assets/logo_etib.png"
import MsgImg from "@/assets/Messages.png"
import CaisseImg from "@/assets/caisseResto.png"
import FactureXImg from "@/assets/facture-x.png"
import TraceurImg from "@/assets/geolocalisation.gif"
import DemoSyncMP4 from "@/assets/Demo-SyncFichiers.mp4"
import DemoCalculItineraireMP4 from "@/assets/Demo-CalculItineraire.mp4"
import ArkanoidImg from "@/assets/Arkanoid.png"
import ArcanorImg from "@/assets/arcanor.jpg"
import CdCImg from "@/assets/Cliqueduclique.jpg"
import LinEpicerie from "@/assets/linepicerie.png"
export default {
    name:'Portfolio',
    components:{
        Realisation
    },
    data(){
        return{
            compagnies:[
                {   
                    id: 1,
                    label: "Chez ",
                    img: GanacosImg,
                    imgWidth: "150px",
                    realisations: [
                        {
                            id: 1,
                            label: "Ajout d'une interface de saisie de couleur existante : spectrum-color-picker",
                            otherText: [],
                            img: SpectrumImg,
                            imgStyle: "",
                            style: "",
                            template: null
                        },
                        {
                            id: 2,
                            label: "Ajout d'un outil d'auto-completion personnalisé",
                            otherText: [],
                            img: AutoCompletionImg,
                            imgStyle: "",
                            style: "",
                            template: null
                        } 
                        ,
                        {
                            id: 3,
                            label: "Développement de plusieurs fonctionnalités sur tableau/matrice généré par l'outil existant handsontable",
                            otherText: [
                                "Ajout d'une ligne de total en colonne",
                                "Surlignage en gras d'une ligne",
                                "Affichage d'une légende des condition de formatage de cellules"
                            ],
                            img: HandsontableImg,
                            imgStyle: "",
                            style: "",
                            template: null
                        } 
                    ]
                },
                {   
                    id: 2,
                    label: "Chez ",
                    img: ProgidysImg,
                    imgWidth: "200px",
                    realisations: [
                        {
                            id: 1,
                            label: "Création d'un outil de messagerie type messenger",
                            otherText: [
                                "Suite au besoin des entreprises à mettre en place le télétravail lors de la crise sanitaire de la COVID19, j’ai réalisé une interface de messagerie intantanée en passant par un service REST."
                            ],
                            img: MsgImg,
                            template: null,
                            imgStyle: "margin-left: 2.7em",
                            style: "width: 20em;"
                        },
                        {
                            id: 2,
                            label: "Calcul de la formule la moins couteuse",
                            otherText: [
                                "L’ERP Progidys intègre un logiciel de caisse qui permet aux restaurateurs de saisir les commandes.",
                                "Le besoin était de créer un bouton qui allait modifier l’agencement des articles (article en menu / hors menu / en supplément…) dans la formule pour, trouver la formule la moins chère.",
                                "Cet algorithme était un réel défi technique car les performances devaient être moindre pour éviter de faire attendre un restaurateur."
                            ],
                            img: CaisseImg,
                            template: null,
                            imgStyle: "width: 30em",
                            style: ""
                        },
                        {
                            id: 3,
                            label: "Generation de Facture-X",
                            otherText: [
                                "Une facture-x est un PDF qui contient en pièce jointe les détails du document sous forme XML. Je devais générer un XML avec les mêmes données placées dans le PDF et, trouver comment ajouter le XML en pièce jointe du PDF généré."
                            ],
                            img: FactureXImg,
                            template: null,
                            imgStyle: "width: 30em",
                            style: ""
                        }
                    ]
                },
                {   
                    id: 3,
                    label: "Chez ",
                    img: ETIBImg,
                    imgWidth: "100px",
                    realisations: [
                        {
                            id: 1,
                            label: "Traceur routier",
                            otherText: [
                                "Certains des clients d’ETIB étaient des groupes de plusieurs chauffeurs de taxi, ambulances… Le manager devait savoir où se trouvent tous ses taxis à tout moment. Un collègue a réalisé une application mobile pour envoyer les coordonnées GPS à un serveur toutes les 30 secondes, j’ai réalisé de mon côté, l’interface pour afficher les taxis sur une carte, les coordonnées étant reçu en base de données"
                            ],
                            img: TraceurImg,
                            template: null,
                            imgStyle: "margin-left: 2.7em; width: 30em",
                            style: ""
                        },
                        {
                            id: 2,
                            label: "Synchronisation de documents",
                            otherText: [
                                "L’entreprise ETIB avaient besoin de rendre le processus d’envoi de documents à leurs clients plus fiables, économiques et rapides. Le processus se faisait par voie postale ou par mail.",
                                "J’ai réalisé dans un premier temps, un programme permettant de synchroniser les documents comptables enregistrés sur un ordinateur, avec un serveur.",
                                "Puis, une application web (hébergé sur le serveur synchronisé) pour donner un accès par authentifications aux clients destinataires. "
                            ],
                            img: null,
                            template: "<video controls><source src='"+DemoSyncMP4+"' type='video/mp4'><p>Votre navigateur ne prend pas en charge les vidéos HTML5.Voici <a href='"+DemoSyncMP4+"'>un lien pour télécharger la vidéo</a>.</p></video>",
                            imgStyle: "margin-left: 2.7em; width: 30em",
                            style: ""
                        },
                        {
                            id: 3,
                            label: "Calcul d’itinéraire ",
                            otherText: [
                                "Les clients d’ETIB avaient besoin de connaitre à l’avance la distance qu’un trajet allait leur demander.",
                                "J’ai comparé plusieurs services de calcul routier, sur la performance, le coût et la fiabilité."
                            ],
                            img: null,
                            template: "<video controls><source src='"+DemoCalculItineraireMP4+"' type='video/mp4'><p>Votre navigateur ne prend pas en charge les vidéos HTML5.Voici <a href='"+DemoCalculItineraireMP4+"'>un lien pour télécharger la vidéo</a>.</p></video>",
                            imgStyle: "margin-left: 2.7em; width: 30em",
                            style: ""
                        },
                    ]
                },
                {   
                    id: 4,
                    label: "Lors de mes formations",
                    img: null,
                    imgWidth: "100px",
                    realisations: [
                        {
                            id: 1,
                            label: "Application de de scan rapide à destination d'une épicerie",
                            otherText: [
                                "Dans le cadre du projet de fin d'année de licence professionnelle, j'ai travaillé dans une équipe de 5 développeur à la réalisation d'une application mobile pour une épicerie de la région de Limoges.",
                                "L'application à été réalisé en kotlin, sur l'IDE AndroidStudio, et le code mis en commun par gestionnaire de version git.",
                                "Le but de l'application était de permettre à l'épicier de scanner plusieurs produits, puis de faire une liste des produits scanner, pour finnalement générer des factures, devis, bon de commandes au format pdf en un clic.",
                                "Je m'occupais de la partie de génération des documents pdf. J'ai utilisé la bibliothèque iText pour écrire dans un pdf."
                            ],
                            img: LinEpicerie,
                            template: null,
                            imgStyle: "width: 20em;margin: 0 5em;",
                            style: "width: 30em"
                        },
                        {
                            id: 2,
                            label: "Réalisation du jeu arcade Arkanoid en JavaScript afin d'apprendre un pattern MVC du languages",
                            otherText: [
                                
                            ],
                            img: ArkanoidImg,
                            template: null,
                            imgStyle: "",
                            style: "width: 30em"
                        },
                        {
                            id: 3,
                            label: "Développemment d'une plateforme web en Laravel",
                            otherText: [
                                "Les universités de bretagne sud (UBS) avaient besoins d'une plateforme pour répertorier et afficher les statistiques de leurs universités (taux de réussite, âge moyen, moyennes...)",
                                "Les besoins portaient sur la création d'une base de données, le développement d'un back office, affichage de graphiques et possibilités de gérer les utilisateurs et leurs droits."
                            ],
                            img: null,
                            template: null,
                            imgStyle: "",
                            style: "width: 30em"
                        },
                        {
                            id: 4,
                            label: "Développement d'un jeu du jeu de société Arcanor en Java et javax.swing",
                            otherText: [
                                "Le jeu à été développé en équipe de 2 développeurs et nous étions en compétitions. Afin de nous démarquer des autres joueurs nous nous sommes inspirés d'un design de jeu d'arcade (car très simples et avec de nombreuses images existantes sur internet).",
                                "Nous avons utilisés une méthode agile, réalisés des cahiers des charges et comptes rendus.",
                                "Dans ce jeu de stratégie à deux, le but est de déplacer ses pièces pour les apporter sur la ligne adverse. A son tour, le joueur choisit entre déplacer l'une de ses pièces, libérer une de ses pièces cachée sous une autre, manger une pièce adverse.  Quand une pièce arrive sur la ligne adverse, elle y reste et est invulnérable. Plus la pièce est petite, plus elle rapporte de point (4 tailles, de 1 à 4 points). Le but étant d'avoir 12 points de pièces arrivées. "
                            ],
                            img: ArcanorImg,
                            template: null,
                            imgStyle: "",
                            style: "width: 30em"
                        },
                        {
                            id: 5,
                            label: "Développement d'un site vitrine avec Wordpress pour l'association la clique du clic",
                            otherText: [
                                "Afin de réaliser un premier projet, nous avons réalisé un site internet en équipe de 2 pour le une association de théâtre d'improvisation.",
                                "Les objectifs étaient d'apprendre à réaliser un cahier des charges, d'organiser des réunions avec un client, apprendre la méthode agile."
                            ],
                            img: CdCImg,
                            template: null,
                            imgStyle: "",
                            style: "width: 30em"
                        }
                    ]
                }
            ]
        } 
    }
}
</script>

<style lang="scss" scoped>

.porfolio{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
}

.realisation{
    background-color: #bbb;
    box-shadow: 6px 5px 5px #737373;
    width: min-content;
    height: min-content;
    border-radius: 10px;
    margin: 1em
}

.resalisation-body{
    padding: 1em 0;
    
}

.compagny-label{
    margin-right: 1em;
    margin-top: auto;
    margin-bottom: auto;
}

.compagny{
    margin: 2em 0
}

.compagny-title{
    margin-left: 5em;
}
</style>