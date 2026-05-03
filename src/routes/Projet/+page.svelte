<script>
    const projects = [
         {
            title: "Émulateur RISC-V ",
            description: "Émulateur de processeur RISC-V complètement fonctionnel en Rust avec support complet de 41 instructions. Dispose d'un mode interactif avec débogage et commandes de visualisation mémoire.",
            image: "./Projet/emulateur.png",
            tags: ["Rust", "Architecture", "Émulation", "Système"],
            link: "https://gitlab.univ-lille.fr/camille.okubo.etu/sae-s5.a.01emulateur",
            skills: "Rust, Cargo, Architecture processeur, Mémoire, Compilation",
            context: "1376 lignes de code Rust - 41 opcodes RV32I implémentés - Mode interactif avec déboguer - 7 modules bien structurés"
        },
        {
            title: "Site gestion de Rendez-vous",
            description: "Application web de gestion de rendez-vous avec système de réservation, gestion des rôles (utilisateur/admin) et paramétrage du planning avancé (jours ouvrés, horaires, créneaux, capacités).",
            image: "./Projet/s5a01.png",
            tags: ["Java", "Spring Boot", "Maven", "Web", "Backend"],
            link: "https://gitlab.univ-lille.fr/camille.okubo.etu/s5a01mathieu",
            skills: "Java 17, Spring Boot, Maven, Gestion utilisateurs, Architecture backend",
            context: "Application complète avec authentification, gestion des rôles, réservations et paramétrage dynamique"
        },
        {
            title: "ChatMoiFort",
            description: "Application de messagerie en ligne développée avec TomCat. Plateforme complète de communication en temps réel avec gestion des utilisateurs.",
            image: "./Projet/ChatMoiFort.png",
            tags: ["Java", "Bootstrap", "CSS", "HTML", "PostgreSQL"],
            link: "https://gitlab.univ-lille.fr/matias.mennecart.etu/sae-r4.01",
            skills: "Java, Bootstrap, CSS, HTML, PostgreSQL"
        },
        {
            title: "Logiciel de Classification",
            description: "Application de classification permettant de charger un jeu de données et le classifier en utilisant l'algorithme k-NN pour l'apprentissage automatique.",
            image: "./Projet/Classification.png",
            tags: ["Java", "Git", "Figma"],
            link: "https://gitlab.univ-lille.fr/sae302/2024/H4_SAE3.3",
            skills: "Java, Git, Figma"
        },
        {
            title: "RentApple",
            description: "Site web fictif d'une plateforme de covoiturage. Solution numérique répondant aux besoins modernes de mobilité partagée.",
            image: "./Projet/rentApple.png",
            tags: ["HTML", "CSS"],
            link: "https://github.com/h2lh-dev/RentApple",
            skills: "HTML, CSS"
        },
        {
            title: "Nuit de l'Info",
            description: "Participation au concours national qui rassemble les étudiants en informatique pour créer une solution numérique innovante.",
            image: "./Projet/nuitInfo.png",
            tags: ["HTML", "CSS", "JavaScript", "Svelte", "Git"],
            link: "https://github.com/h2lh-dev/HDFC",
            website: "hdfc-beige.vercel.app",
            skills: "HTML, CSS, JavaScript, Svelte, Git"
        },
        {
            title: "PirAttack",
            description: "Jeu simple développé en 5 jours avec la méthodologie Agile. Projet de rentrée mettant en avant le travail en équipe et la gestion de projet.",
            image: "./Projet/pirAttack.png",
            tags: ["Java", "Git"],
            link: "https://gitlab.univ-lille.fr/2024-projet-agile-de-rentree/groupe-7",
            skills: "Java, Git"
        },
        {
            title: "SAM - Routeur d'itinéraires",
            description: "Application permettant de choisir le meilleur itinéraire selon les critères (temps, prix, écologie). Utilise l'algorithme de Dijkstra.",
            image: "./Projet/SAM.png",
            tags: ["Java", "Git"],
            link: "https://gitlab.univ-lille.fr/sae2.01-2.02/2024/B1",
            skills: "Java, Git"
        },
        {
            title: "Java Daiquiri Dash",
            description: "Jeu éducatif créé sur Genially présentant les bases du fonctionnement de Java de manière interactive et ludique.",
            image: "./Projet/javaDaiquiriDash.png",
            tags: ["Genially", "Éducatif"],
            skills: "Genially"
        },
        {
            title: "Base de données Parcoursup",
            description: "Ventilation d'un jeu de données Parcoursup sur PostgreSQL. Réalisation de requêtes SQL avancées pour des analyses statistiques.",
            image: "./Projet/parcoursup.png",
            tags: ["PostgreSQL", "SQL"],
            skills: "PostgreSQL, SQL"
        },
        {
            title: "Création Machine Virtuelle",
            description: "Création et configuration d'une machine virtuelle avec Debian 12. Installation et optimisation de l'OS pour une utilisation agréable.",
            image: "./Projet/virtualbox-main.png",
            tags: ["Linux", "VirtualBox", "Debian"],
            skills: "Linux, VirtualBox, Debian"
        }
    ];
</script>

<section class="projects-section">
    <div class="projects-header">
        <h1>Mes Projets</h1>
        <p>Découvrez les différents projets que j'ai réalisés durant ma formation et mes initiatives personnelles</p>
    </div>

    <div class="projects-grid">
        {#each projects as project (project.title)}
            <div class="project-card">
                <div class="project-image">
                    <img src={project.image} alt={project.title} />
                    <div class="project-overlay">
                        {#if project.link}
                            <a href={project.link} target="_blank" class="project-link">Voir le code</a>
                        {/if}
                        {#if project.website}
                            <a href={`https://${project.website}`} target="_blank" class="project-link">Visiter</a>
                        {/if}
                    </div>
                </div>
                <div class="project-content">
                    <h3>{project.title}</h3>
                    <p>{project.description}</p>
                    {#if project.context}
                        <p class="project-context">{project.context}</p>
                    {/if}
                    <div class="project-tags">
                        {#each project.tags as tag}
                            <span class="tag">{tag}</span>
                        {/each}
                    </div>
                </div>
            </div>
        {/each}
    </div>
</section>

<style>
    .projects-section {
        max-width: 1400px;
        margin: 0 auto;
        padding: 0 20px;
    }

    .projects-header {
        text-align: center;
        margin-bottom: 80px;
    }

    .projects-header h1 {
        font-size: 48px;
        margin-bottom: 20px;
        background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .projects-header p {
        font-size: 18px;
        color: #94a3b8;
        max-width: 600px;
        margin: 0 auto;
    }

    .projects-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(330px, 1fr));
        gap: 30px;
        margin-bottom: 60px;
    }

    .project-card {
        background: rgba(30, 41, 59, 0.6);
        border: 1px solid rgba(96, 165, 250, 0.2);
        border-radius: 15px;
        overflow: hidden;
        transition: all 0.3s ease;
        display: flex;
        flex-direction: column;
        height: 100%;
    }

    .project-card:hover {
        border-color: rgba(96, 165, 250, 0.5);
        box-shadow: 0 20px 50px rgba(59, 130, 246, 0.15);
        transform: translateY(-8px);
    }

    .project-image {
        position: relative;
        width: 100%;
        height: 200px;
        overflow: hidden;
        background: linear-gradient(135deg, rgba(59, 130, 246, 0.1), rgba(139, 92, 246, 0.1));
    }

    .project-image img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        transition: transform 0.3s ease;
    }

    .project-card:hover .project-image img {
        transform: scale(1.05);
    }

    .project-overlay {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background: rgba(15, 23, 42, 0.8);
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 15px;
        opacity: 0;
        transition: opacity 0.3s ease;
        backdrop-filter: blur(4px);
    }

    .project-card:hover .project-overlay {
        opacity: 1;
    }

    .project-link {
        display: inline-block;
        padding: 10px 24px;
        background: linear-gradient(135deg, #3b82f6 0%, #8b5cf6 100%);
        color: white;
        border-radius: 8px;
        font-weight: 600;
        font-size: 14px;
        transition: all 0.3s ease;
    }

    .project-link:hover {
        transform: translateY(-2px);
        box-shadow: 0 8px 20px rgba(59, 130, 246, 0.4);
    }

    .project-content {
        padding: 30px;
        flex-grow: 1;
        display: flex;
        flex-direction: column;
    }

    .project-content h3 {
        font-size: 22px;
        margin-bottom: 12px;
        color: #60a5fa;
    }

    .project-content p {
        color: #cbd5e1;
        font-size: 14px;
        line-height: 1.8;
        margin-bottom: 20px;
        flex-grow: 1;
    }

    .project-tags {
        display: flex;
        flex-wrap: wrap;
        gap: 8px;
    }

    .tag {
        display: inline-block;
        padding: 6px 14px;
        background: rgba(96, 165, 250, 0.15);
        color: #60a5fa;
        border-radius: 20px;
        font-size: 12px;
        font-weight: 500;
        border: 1px solid rgba(96, 165, 250, 0.3);
        transition: all 0.3s ease;
    }

    .tag:hover {
        background: rgba(96, 165, 250, 0.25);
        border-color: rgba(96, 165, 250, 0.6);
    }

    .project-context {
        font-size: 12px !important;
        color: #94a3b8 !important;
        background: rgba(96, 165, 250, 0.05) !important;
        border-left: 2px solid #60a5fa;
        padding: 10px 12px !important;
        margin-bottom: 15px !important;
        border-radius: 4px;
        line-height: 1.5 !important;
    }

    @media (max-width: 768px) {
        .projects-header h1 {
            font-size: 36px;
        }

        .projects-grid {
            grid-template-columns: 1fr;
        }

        .project-overlay {
            opacity: 1;
        }

        .project-link {
            padding: 8px 20px;
            font-size: 13px;
        }
    }
</style>



