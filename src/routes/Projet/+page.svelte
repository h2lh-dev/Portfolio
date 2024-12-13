
<body>
<div class="portfolio">
    <div class="project">
        <img src="projet1.jpg" alt="Projet 1">
        <div class="project-info">
            <h2>Projet 1</h2>
            <p>Description du projet 1.</p>
        </div>
    </div>
    <div class="project">
        <img src="projet2.jpg" alt="Projet 2">
        <div class="project-info">
            <h2>Projet 2</h2>
            <p>Description du projet 2.</p>
        </div>
    </div>
    <div class="project">
        <img src="projet3.jpg" alt="Projet 3">
        <div class="project-info">
            <h2>Projet 3</h2>
            <p>Description du projet 3.</p>
        </div>
    </div>
    <!-- Ajoute d'autres projets ici -->
</div>
</body>

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
    .project img {
        width: 100%; /* L'image occupe toute la largeur de la page */
        height: auto; /* L'image garde ses proportions */
        display: block;
    }

    /* Informations du projet */
    .project-info {
        padding: 15px;
    }

    .project-info h2 {
        font-size: 1.5rem;
        margin-bottom: 10px;
    }

    .project-info p {
        font-size: 1rem;
        color: #666;
    }

</style>



