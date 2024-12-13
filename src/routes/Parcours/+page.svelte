<script>
    const timeline = [

        { date: "Avril 2025 - Juin 2025", title: "Stage AnankéInc", description: "Stage Eramus au Canada", side: "left" },
        { date: "2022 - 2026", title: "BUT Informatique", description: "IUT A Villeneuve d'Ascq - Université de Lille" , side:"right"},
        { date: "2019 - 2022", title: "Baccalauréat sciences et technologies de l'industrie et du développement durable", description: "Lycées Général et Technologique & Professionnel Edmond Labbé - Douai", side: "right"},

    ];
</script>

<div class="timeline">
    {#each timeline as event}
        <div class="timeline-item {event.side}">
            <div class="timeline-marker"></div>
            <div class="timeline-content">
                <h3>{event.date}</h3>
                <h4>{event.title}</h4>
                <p>{event.description}</p>
            </div>
        </div>
    {/each}
</div>

<style>
    .timeline {
        position: relative;
        margin: 0 auto;
        padding: 20px 0;
        width: 80%; /* Ajuste selon tes besoins */
        max-width: 800px;
    }

    .timeline:before {
        content: "";
        position: absolute;
        top: 0;
        bottom: 0;
        left: 50%; /* Ligne centrale alignée */
        width: 4px; /* Épaisseur de la ligne */
        background-color: #007bff; /* Couleur de la ligne */
        transform: translateX(-50%);
    }

    .timeline-item {
        position: relative;
        margin-bottom: 40px;
    }

    .timeline-marker {
        position: absolute;
        left: 50%; /* Centré sur la ligne */
        top: 0; /* Place le point au début de chaque événement */
        width: 20px; /* Taille du point */
        height: 20px; /* Taille du point */
        background-color: #007bff; /* Couleur du point */
        border: 2px solid #fff; /* Ajoute un contour blanc */
        border-radius: 50%; /* Cercle parfait */
        transform: translateX(-50%); /* Centrer horizontalement */
    }

    .timeline-content {
        position: relative;
        padding: 10px 15px;
        background: #f9f9f9;
        border-radius: 8px;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        max-width: 300px;
    }

    .timeline-item.left {
        text-align: right;
        margin-left: 0;
        margin-right: calc(50% + 40px); /* Place le contenu à gauche de la ligne */
    }

    .timeline-item.right {
        text-align: left;
        margin-left: calc(50% + 40px); /* Place le contenu à droite de la ligne */
        margin-right: 0;
    }

    .timeline-content h3 {
        margin: 0 0 5px;
        font-size: 16px;
        color: #007bff;
    }

    .timeline-content h4 {
        margin: 0;
        font-size: 14px;
        font-weight: normal;
        color: #333;
    }

    .timeline-content p {
        margin: 5px 0 0;
        font-size: 12px;
        color: #555;
    }


</style>