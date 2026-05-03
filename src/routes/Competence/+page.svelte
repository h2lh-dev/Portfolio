<script>
    const competences = [
        {
            category: "Frontend",
            skills: [
                { name: "HTML", icon: "html", level: 90 },
                { name: "CSS", icon: "css", level: 85 },
                { name: "JavaScript", icon: "javascript", level: 85 },
                { name: "Tailwind CSS", icon: "tailwind", level: 80 },
                { name: "Svelte", icon: "svelte", level: 75 }
            ]
        },
        {
            category: "Backend",
            skills: [
                { name: "PHP/Laravel", icon: "php", level: 85 },
                { name: "PostgreSQL", icon: "postgresql", level: 80 },
                { name: "API REST", icon: "api", level: 80 },
                { name: "Java", icon: "java", level: 75 },
                { name: "Linux", icon: "linux", level: 75 }
            ]
        },
        {
            category: "DevOps & Outils",
            skills: [
                { name: "Git", icon: "git", level: 85 },
                { name: "Figma", icon: "figma", level: 75 },
                { name: "Agile/Scrum", icon: "agile", level: 75 },
                { name: "JetBrains Tools", icon: "idea", level: 80 }
            ]
        }
    ];

    const softSkillsAnalysis = [
        {
            category: "Manière d'être",
            skills: [
                {
                    name: "Autonomie et responsabilité",
                    description: "Capacité à gérer un projet complet de bout en bout sans supervision constante",
                    professional: "Gestion complète du projet de création de polls chez AnankéInc, avec prise de décisions architecturales",
                    reflection: "Je me sens plus confiant quand j'ai une vision claire mais de la liberté pour l'exécution. L'autonomie me motive, mais j'ai besoin de feedbacks réguliers pour valider ma direction."
                },
                {
                    name: "Adaptabilité",
                    description: "Capacité à s'adapter rapidement à de nouveaux environnements et contextes",
                    professional: "Stage international, petite équipe, stack technologique nouvelle, méthodologie Agile rapide - adaptation réussie",
                    reflection: "J'apprends mieux en faisant qu'en étudiant. Cette expérience m'a montré que je peux maîtriser rapidement de nouveaux outils quand ils servent un objectif concret."
                },
                {
                    name: "Engagement et sens des responsabilités",
                    description: "Implication personnelle dans la qualité du travail livré",
                    professional: "Prise en charge complète de la qualité du code et de la fonctionnalité, avec attention aux détails utilisateur",
                    reflection: "Je m'engage vraiment quand je comprends l'impact de mon travail. Voir le projet utilisé et apprécié me motive fortement."
                },
                {
                    name: "Gestion du stress et des émotions",
                    description: "Maintien de la performance sous pression",
                    professional: "Délais serrés, attentes claires, environnement startup - gestion efficace du stress par organisation et priorités",
                    reflection: "Le stress me pousse à être efficace quand j'ai un plan. J'ai découvert que j'aime les deadlines courtes car elles forcent la focus."
                },
                {
                    name: "Confiance en soi",
                    description: "Capacité à croire en ses compétences et à les démontrer",
                    professional: "Confiance progressive avec chaque feature développée, capacité à présenter le travail sans crainte",
                    reflection: "Ma confiance vient de la compétence. Plus je maîtrise un domaine, plus je suis confiant. J'ai besoin de pratiquer pour être sûr de moi."
                }
            ]
        },
        {
            category: "Manière de communiquer",
            skills: [
                {
                    name: "Communication orale et écrite",
                    description: "Capacité à exprimer ses idées clairement en contexte professionnel",
                    professional: "Daily standups, présentations du projet, discussions techniques avec l'équipe en anglais (contexte international)",
                    reflection: "Je maîtrise mieux la communication écrite que l'oral. Je dois progresser sur la fluidité de la communication orale en situation de présentation."
                },
                {
                    name: "Écoute et reformulation",
                    description: "Capacité à comprendre les besoins des autres et les reformuler",
                    professional: "Écoute des retours du fondateur sur les features, reformulation des besoins utilisateur en spécifications techniques",
                    reflection: "Je pose souvent trop rapidement des solutions. Je dois prendre plus de temps pour bien comprendre avant de proposer."
                },
                {
                    name: "Assertivité",
                    description: "Capacité à exprimer son point de vue de manière respectueuse mais claire",
                    professional: "Discussions techniques sur les choix d'architecture, propositions d'améliorations sans crainte du feedback",
                    reflection: "Je suis capable d'être assertif techniquement, mais parfois j'hésite trop avant de partager mon avis sur des sujets non-techniques."
                },
                {
                    name: "Réception du feedback",
                    description: "Capacité à recevoir les critiques constructivement et à progresser",
                    professional: "Code reviews régulières, retours du tuteur, amélioration continue basée sur les feedbacks",
                    reflection: "J'accueille bien le feedback quand il est constructif. Je dois mieux différencier critique du travail et critique personnelle."
                }
            ]
        },
        {
            category: "Manière de travailler avec les autres",
            skills: [
                {
                    name: "Travail en équipe",
                    description: "Capacité à collaborer efficacement avec les autres",
                    professional: "Petite équipe de 3 personnes, partage de connaissances, support mutuel, coordination sur les livrables",
                    reflection: "J'aime les petites équipes où chacun a un rôle clair. Je préfère la qualité de la collaboration à la taille du groupe."
                },
                {
                    name: "Coopération",
                    description: "Contribution volontaire aux objectifs du groupe",
                    professional: "Help au-delà du périmètre strict quand l'équipe en avait besoin, partage de solutions et d'apprentissages",
                    reflection: "Je coopère naturellement quand je sens que c'est un effort collectif vers un but commun."
                },
                {
                    name: "Gestion des désaccords",
                    description: "Capacité à naviguer les tensions constructivement",
                    professional: "Discussions techniques respectueuses, recherche de consensus basée sur les données et l'expérience",
                    reflection: "Je préfère discuter ouvertement plutôt que d'éviter. J'ai appris que écouter l'autre argument m'aidait souvent à trouver une meilleure solution."
                },
                {
                    name: "Prise d'initiative",
                    description: "Capacité à proposer et mener des actions nouvelles",
                    professional: "Propositions d'optimisations, prise d'initiative sur certaines features, leadership technique sur certains choix",
                    reflection: "Je prends l'initiative naturellement quand je vois une amélioration possible. C'est devenu un point fort mais je dois rester attentif à ne pas surcharger."
                }
            ]
        }
    ];
</script>

<section class="competences-section">
    <div class="competences-header">
        <h1>Mes Compétences</h1>
        <p>Hard skills techniques et soft skills développées en contexte professionnel</p>
    </div>

    <div class="competences-container">
        <!-- Hard Skills Section -->
        <div class="hard-skills-section">
            <h2>Compétences Techniques (Hard Skills)</h2>
            <p class="section-intro">Langages, frameworks et outils maîtrisés grâce à mon expérience chez AnankéInc et ma formation</p>

            <div class="skills-grid">
                {#each competences as category (category.category)}
                    <div class="skills-category">
                        <h3>{category.category}</h3>
                        <div class="skills-list">
                            {#each category.skills as skill}
                                <div class="skill-card">
                                    <div class="skill-header">
                                        <span class="skill-name">{skill.name}</span>
                                        <span class="skill-level">{skill.level}%</span>
                                    </div>
                                    <div class="progress-bar">
                                        <div class="progress-fill" style="width: {skill.level}%"></div>
                                    </div>
                                </div>
                            {/each}
                        </div>
                    </div>
                {/each}
            </div>
        </div>

        <!-- Soft Skills Section -->
        <div class="soft-skills-section">
            <h2>Compétences Comportementales (Soft Skills)</h2>
            <p class="section-intro">Analyse réflexive de mes compétences humaines développées en situation professionnelle réelle</p>

            <div class="soft-skills-container">
                {#each softSkillsAnalysis as category (category.category)}
                    <div class="category-section">
                        <h3 class="category-title">{category.category}</h3>
                        <div class="soft-skills-list">
                            {#each category.skills as skill}
                                <div class="soft-skill-card">
                                    <div class="skill-title-section">
                                        <h4>{skill.name}</h4>
                                        <p class="skill-short-desc">{skill.description}</p>
                                    </div>

                                    <div class="skill-details">
                                        <div class="detail-box">
                                            <h5>En contexte professionnel</h5>
                                            <p>{skill.professional}</p>
                                        </div>

                                        <div class="detail-box reflection-box">
                                            <h5>Réflexion personnelle</h5>
                                            <p>{skill.reflection}</p>
                                        </div>
                                    </div>
                                </div>
                            {/each}
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </div>
</section>

<style>
    .competences-section {
        max-width: 1400px;
        margin: 0 auto;
        padding: 0 20px;
    }

    .competences-header {
        text-align: center;
        margin-bottom: 80px;
    }

    .competences-header h1 {
        font-size: 48px;
        margin-bottom: 20px;
        background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .competences-header p {
        font-size: 18px;
        color: #94a3b8;
    }

    .competences-container {
        display: flex;
        flex-direction: column;
        gap: 100px;
    }

    .hard-skills-section,
    .soft-skills-section {
        padding: 60px 40px;
        background: rgba(30, 41, 59, 0.4);
        border: 1px solid rgba(96, 165, 250, 0.2);
        border-radius: 20px;
    }

    .hard-skills-section h2,
    .soft-skills-section h2 {
        font-size: 32px;
        color: #60a5fa;
        margin: 0 0 15px 0;
    }

    .section-intro {
        color: #94a3b8;
        font-size: 15px;
        margin: 0 0 40px 0;
    }

    .skills-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 30px;
    }

    .skills-category {
        background: rgba(30, 41, 59, 0.6);
        border: 1px solid rgba(96, 165, 250, 0.2);
        border-radius: 15px;
        padding: 30px;
        transition: all 0.3s ease;
    }

    .skills-category:hover {
        border-color: rgba(96, 165, 250, 0.5);
        box-shadow: 0 10px 30px rgba(59, 130, 246, 0.1);
        transform: translateY(-3px);
    }

    .skills-category h3 {
        font-size: 18px;
        color: #60a5fa;
        margin: 0 0 25px 0;
    }

    .skills-list {
        display: flex;
        flex-direction: column;
        gap: 20px;
    }

    .skill-card {
        display: flex;
        flex-direction: column;
        gap: 8px;
    }

    .skill-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .skill-name {
        color: #e2e8f0;
        font-weight: 500;
        font-size: 14px;
    }

    .skill-level {
        color: #60a5fa;
        font-size: 13px;
        font-weight: 600;
    }

    .progress-bar {
        width: 100%;
        height: 6px;
        background: rgba(96, 165, 250, 0.1);
        border-radius: 3px;
        overflow: hidden;
    }

    .progress-fill {
        height: 100%;
        background: linear-gradient(90deg, #3b82f6, #8b5cf6);
        border-radius: 3px;
        transition: width 0.6s ease;
    }

    .soft-skills-container {
        display: flex;
        flex-direction: column;
        gap: 60px;
    }

    .category-section {
        margin-bottom: 20px;
    }

    .category-title {
        font-size: 24px;
        color: #60a5fa;
        margin: 0 0 30px 0;
        padding-bottom: 15px;
        border-bottom: 2px solid rgba(96, 165, 250, 0.2);
    }

    .soft-skills-list {
        display: grid;
        gap: 25px;
    }

    .soft-skill-card {
        background: rgba(30, 41, 59, 0.6);
        border: 1px solid rgba(96, 165, 250, 0.2);
        border-radius: 15px;
        padding: 30px;
        transition: all 0.3s ease;
    }

    .soft-skill-card:hover {
        border-color: rgba(96, 165, 250, 0.5);
        box-shadow: 0 10px 30px rgba(59, 130, 246, 0.1);
        transform: translateY(-2px);
    }

    .skill-title-section h4 {
        font-size: 20px;
        color: #e2e8f0;
        margin: 0 0 8px 0;
    }

    .skill-short-desc {
        color: #94a3b8;
        font-size: 14px;
        margin: 0 0 20px 0;
        font-weight: 500;
    }

    .skill-details {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 20px;
    }

    .detail-box {
        background: rgba(96, 165, 250, 0.05);
        border-left: 3px solid #60a5fa;
        padding: 20px;
        border-radius: 8px;
    }

    .detail-box h5 {
        color: #60a5fa;
        font-size: 13px;
        text-transform: uppercase;
        letter-spacing: 1px;
        margin: 0 0 10px 0;
    }

    .detail-box p {
        color: #cbd5e1;
        font-size: 14px;
        line-height: 1.7;
        margin: 0;
    }

    .reflection-box {
        background: rgba(139, 92, 246, 0.05);
        border-left-color: #a78bfa;
    }

    .reflection-box h5 {
        color: #a78bfa;
    }

    @media (max-width: 768px) {
        .competences-header h1 {
            font-size: 36px;
        }

        .hard-skills-section h2,
        .soft-skills-section h2 {
            font-size: 26px;
        }

        .skills-grid {
            grid-template-columns: 1fr;
        }

        .skill-details {
            grid-template-columns: 1fr;
        }

        .hard-skills-section,
        .soft-skills-section {
            padding: 30px 20px;
        }

        .category-title {
            font-size: 20px;
        }
    }
</style>
