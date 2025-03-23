<script>

</script>



<div class="portfolio">
    <div class="project">
        <img src="./Projet/ChatMoiFort.png" alt="Projet 2">
        <div class="project-info">
            <h2>ChatMoiFort</h2>
            <p>Dans le cadre de ce projet, nous avons dû réaliser une application de messagerie en ligne. En utilisant TomCat.</p>
            <a href="https://gitlab.univ-lille.fr/matias.mennecart.etu/sae-r4.01"> Git </a>
            <img src="https://skillicons.dev/icons?i=java,bootstrap,css,html,postgresql&theme=dark&perline=15" alt="My Skills" />
        </div>
    </div>
    <div class="project">
        <img src="./Projet/Classification.png" alt="Projet 2">
        <div class="project-info">
            <h2>Logiciel de Classifcation</h2>
            <p>Dans le cadre de ce projet, nous avons dû réaliser une application de classification permettant de charger un jeu de données et de le classifier en utilisant l'algorithme k-NN.</p>
            <a href="https://gitlab.univ-lille.fr/sae302/2024/H4_SAE3.3"> Git </a>
            <img src="https://skillicons.dev/icons?i=java,git,figma&theme=dark&perline=15" alt="My Skills" />
        </div>
    </div>
    <div class="project">
        <img src="./Projet/rentApple.png" alt="Projet 2">
        <div class="project-info">
            <h2>RentApple</h2>
            <p>Dans le cadre de ce projet, nous avons dû réaliser le site web fictif d'une entreprise en répondant à un besoin de création d'une plateforme de covoiturage.</p>
            <a href="https://github.com/h2lh-dev/RentApple"> Git </a>
           <img src="https://skillicons.dev/icons?i=html,css&theme=dark&perline=15" alt="My Skills" />
        </div>
    </div>
    <div class="project">
        <img src="./Projet/nuitInfo.png" alt="Projet 2">
        <div class="project-info">
            <h2>Nuit de l'info</h2>
            <p>La Nuit de l'Info est un concours national qui rassemble les étudiants en informatique pour la création en équipe d'un site web proposant une solution numérique à des problématiques réelles.</p>
            <a href="https://github.com/h2lh-dev/HDFC"> Git </a>
            <a href="hdfc-beige.vercel.app"> Lien </a>
            <img src="https://skillicons.dev/icons?i=html,css,javascript,svelte,git&theme=dark&perline=15" alt="My Skills" />
        </div>
    </div>
    <div class="project">
        <img src="./Projet/pirAttack.png" alt="Projet 2">
        <div class="project-info">
            <h2>PirAttack</h2>
            <p>Nous avons dû réaliser un projet en 5 jours portant sur la création d'un jeu simple en Java, en utilisant la méthodologie Agile.</p>
            <a href="https://gitlab.univ-lille.fr/2024-projet-agile-de-rentree/groupe-7"> Git </a>
            <img src="https://skillicons.dev/icons?i=java,git&theme=dark&perline=15" alt="My Skills" />
        </div>
    </div>
    <div class="project">
        <img src="./Projet/SAM.png" alt="Projet 2">
        <div class="project-info">
            <h2>Sam</h2>
            <p>Nous avons dû créer une application permettant de choisir le meilleur itinéraire en répondant aux critères de la personne (temps, prix et écologie). Nous avons utilisé l'algorithme de Dijkstra.</p>
            <a href="https://gitlab.univ-lille.fr/sae2.01-2.02/2024/B1"> Git </a>
            <img src="https://skillicons.dev/icons?i=java,git&theme=dark&perline=15" alt="My Skills" />
        </div>
    </div>
    <div class="project">
        <img src="./Projet/javaDaiquiriDash.png" alt="Projet 2">
        <div class="project-info">
            <h2>Java Daiquiri Dash</h2>
            <p>Nous avons dû créer un jeu sur le site Genially, qui devait être éducatif, sur le thème de Java, en présentant les bases de son fonctionnement.</p>

            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/85/Genially_%282023%29_logotipo.png/640px-Genially_%282023%29_logotipo.png" alt="My Skills" />

        </div>
    </div>
    <div class="project">
        <img src="./Projet/parcoursup.png" alt="Projet 2">
        <div class="project-info">
            <h2>Base de donnée Parcoursup</h2>
            <p>Nous avons dû ventiler un jeu de données représentant les résultats de Parcoursup sur PostgreSQL et répondre à des questions statistiques à l'aide de requêtes SQL.</p>


            <img src="https://skillicons.dev/icons?i=postgresql&theme=light&perline=15" alt="My Skills" />

        </div>
    </div>

    <div class="project">
        <img src="./Projet/virtualbox-main.png" alt="Projet 2">
        <div class="project-info">
            <h2>Creation Machine Virtuel</h2>
            <p>Nous avons dû créer une machine virtuelle, installer l'OS Debian 12, puis le configurer pour une utilisation agréable.</p>

            <img src="https://upload.wikimedia.org/wikipedia/commons/d/d5/Virtualbox_logo.png" alt="My Skills" />

        </div>
    </div>

    <!-- Ajoute d'autres projets ici -->
</div>


<style>
    /* Réinitialisation des marges et du padding */
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    /* Styles généraux */
    body {
        font-family: Arial, sans-serif;
        line-height: 1.6;
        background-color: #f4f4f4;
    }

    /* Conteneur des projets */
    .portfolio {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); /* Responsive, chaque projet aura au minimum 300px */
        gap: 20px; /* Espacement entre les projets */
        padding: 20px;
    }

    /* Style des projets */
    .project {
        background-color: #fff;
        border-radius: 8px;
        overflow: hidden; /* Pour éviter que l'image dépasse */
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }

    /* Image du projet */
    .project>img {
        width: 100%; /* L'image occupe toute la largeur de la page */
        height: 12vw;/* L'image garde ses proportions */
        object-fit: cover;
        display: block;
    }

    /* Informations du projet */
    .project-info {
        padding: 15px;
        display: flex;
        align-items: center;
        justify-content: space-evenly;
        flex-direction: column;

    }

    .project-info h2 {
        font-size: 1.5rem;
        margin-bottom: 10px;
    }

    .project-info p {
        font-size: 1rem;
        color: #666;
    }

    .project-info img {
        height: 60px;

    }
</style>



