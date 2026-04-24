<script>
    const experience = {
        company: "AnankéInc",
        location: "Canada (Erasmus)",
        period: "Avril 2025 - Juin 2025",
        duration: "3 mois",
        context: "Startup canadienne de 3 personnes spécialisée dans les solutions numériques innovantes",
        role: "Développeur Full Stack",
        missions: [
            {
                title: "Conception et développement d'une plateforme de création de polls",
                description: "Création d'une application web permettant aux utilisateurs de créer, gérer et analyser des sondages en temps réel.",
                context: "Projet principal du stage, réalisé en semi-autonomie",
                scope: [
                    "Architecture de l'application complète (Backend + Frontend)",
                    "Mise en place de la base de données",
                    "Design et implémentation de l'interface utilisateur",
                    "Intégration des fonctionnalités avancées (authentification, real-time updates)"
                ],
                autonomy: "Semi-autonomie avec directives",
                results: "Application fonctionnelle et déployée, respectant les spécifications initiales"
            }
        ],
        teamInteraction: "Équipe de 3 personnes - collaboration régulière avec le fondateur et un autre développeur pour les décisions architecturales et les code reviews",
        hardSkills: [
            { skill: "PHP / Laravel", level: "Avancé", context: "Framework backend principal pour l'application" },
            { skill: "JavaScript", level: "Avancé", context: "Logique frontend et interactions utilisateur" },
            { skill: "Tailwind CSS", level: "Intermédiaire", context: "Styling et responsive design" },
            { skill: "PostgreSQL", level: "Intermédiaire", context: "Conception et gestion de la base de données" },
            { skill: "Git / Versioning", level: "Intermédiaire", context: "Collaboration et gestion du code" },
            { skill: "API REST", level: "Avancé", context: "Création d'APIs pour la communication Frontend-Backend" },
            { skill: "Méthodologie Agile", level: "Intermédiaire", context: "Sprints courts et feedback régulier" }
        ],
        softSkills: [
            {
                skill: "Autonomie et responsabilité",
                description: "Gestion complète d'un projet en semi-autonomie",
                situation: "J'ai dû gérer seul le développement complet tout en respectant les directives données et les délais. Cela m'a permis de prendre des initiatives tout en restant aligné avec la vision globale."
            },
            {
                skill: "Adaptabilité et apprentissage rapide",
                description: "Maîtrise rapide de nouvelles technologies en contexte professionnel",
                situation: "Je n'avais pas d'expérience préalable intensive avec Laravel. J'ai dû apprendre rapidement en autodidacte en lisant la documentation, regardant des tutoriels et en pratiquant directement sur le projet."
            },
            {
                skill: "Communication et collaboration",
                description: "Travail efficace dans une petite équipe distribuée",
                situation: "Dans une équipe de 3 personnes, la communication était essentielle. Des daily standups courts et des code reviews régulières ont assuré l'alignement et la qualité du code."
            },
            {
                skill: "Gestion du stress et des délais",
                description: "Capacité à livrer dans un contexte de délais rapides",
                situation: "Les sprints courts et les deadlines serrées m'ont appris à prioriser, organiser mon travail et maintenir la qualité sous pression."
            }
        ],
        selfReflection: {
            strengths: [
                "Autonomie: Je suis capable de prendre l'initiative et de gérer un projet complet sans supervision constante",
                "Curiosité: J'apprends rapidement et je ne crains pas d'explorer de nouvelles technologies",
                "Pragmatisme: Je me concentre sur la livraison de solutions fonctionnelles plutôt que sur la perfection",
                "Adaptabilité: Contexte international, petite équipe, méthodologie rapide - je m'adapte rapidement"
            ],
            areasForGrowth: [
                "Documentation: Je dois améliorer la documentation de mon code pour faciliter la maintenance",
                "Tests: Il faut que je sois plus rigoureux sur les tests unitaires et d'intégration",
                "Communication technique: Expliquer des concepts techniques de manière claire reste un défi",
                "Planification à long terme: Je me concentre souvent sur le court terme, j'aimerais développer une vision plus globale"
            ],
            workingStyle: "Je travaille mieux en équipe restreinte avec des objectifs clairs. J'aime avoir de l'autonomie mais aussi du feedback régulier. Je préfère apprendre en faisant plutôt qu'en lisant de la théorie."
        }
    };

    const hardSkillCategories = [
        { category: "Backend", skills: ["PHP/Laravel", "API REST", "PostgreSQL"] },
        { category: "Frontend", skills: ["JavaScript", "Tailwind CSS"] },
        { category: "DevOps & Tools", skills: ["Git/Versioning", "Méthodologie Agile"] }
    ];
</script>

<section class="experience-section">
    <div class="experience-container">
        <h1>Mon Expérience Professionnelle</h1>
        <p class="subtitle">Stage Erasmus chez AnankéInc - Développeur Full Stack</p>

        <div class="experience-header">
            <div class="header-info">
                <h2>{experience.company}</h2>
                <p class="company-context">{experience.context}</p>
                <div class="meta">
                    <span class="meta-item">📍 {experience.location}</span>
                    <span class="meta-item">📅 {experience.period}</span>
                    <span class="meta-item">⏱️ {experience.duration}</span>
                </div>
            </div>
            <div class="header-role">
                <span class="role-badge">{experience.role}</span>
            </div>
        </div>

        <div class="main-mission">
            <h3>Projet Principal</h3>
            <div class="mission-card">
                <h4>{experience.missions[0].title}</h4>
                <p class="mission-description">{experience.missions[0].description}</p>

                <div class="mission-details">
                    <div class="detail-block">
                        <h5>Contexte</h5>
                        <p>{experience.missions[0].context}</p>
                    </div>

                    <div class="detail-block">
                        <h5>Responsabilités</h5>
                        <ul>
                            {#each experience.missions[0].scope as item}
                                <li>{item}</li>
                            {/each}
                        </ul>
                    </div>

                    <div class="detail-block">
                        <h5>Autonomie</h5>
                        <p>{experience.missions[0].autonomy}</p>
                    </div>

                    <div class="detail-block">
                        <h5>Résultats</h5>
                        <p>{experience.missions[0].results}</p>
                    </div>
                </div>
            </div>
        </div>

        <div class="team-section">
            <h3>Intégration à l'équipe</h3>
            <p class="team-text">{experience.teamInteraction}</p>
        </div>

        <div class="hard-skills-section">
            <h3>Compétences Techniques Acquises</h3>
            <div class="skills-grid">
                {#each hardSkillCategories as category}
                    <div class="skills-category">
                        <h4>{category.category}</h4>
                        <div class="skills-list">
                            {#each category.skills as skillName}
                                {#each experience.hardSkills as skill}
                                    {#if skill.skill === skillName}
                                        <div class="skill-item">
                                            <div class="skill-header">
                                                <span class="skill-name">{skill.skill}</span>
                                                <span class="skill-level">{skill.level}</span>
                                            </div>
                                            <p class="skill-context">{skill.context}</p>
                                        </div>
                                    {/if}
                                {/each}
                            {/each}
                        </div>
                    </div>
                {/each}
            </div>
        </div>

        <div class="soft-skills-section">
            <h3>Compétences Comportementales Développées</h3>
            <div class="soft-skills-grid">
                {#each experience.softSkills as skill}
                    <div class="soft-skill-card">
                        <h4>{skill.skill}</h4>
                        <p class="soft-skill-desc">{skill.description}</p>
                        <div class="situation-block">
                            <p><strong>Situation concrète:</strong></p>
                            <p>{skill.situation}</p>
                        </div>
                    </div>
                {/each}
            </div>
        </div>

        <div class="reflection-section">
            <h3>Réflexion et Apprentissages</h3>

            <div class="reflection-grid">
                <div class="reflection-card">
                    <h4>Points Forts Identifiés</h4>
                    <ul>
                        {#each experience.selfReflection.strengths as strength}
                            <li>{strength}</li>
                        {/each}
                    </ul>
                </div>

                <div class="reflection-card">
                    <h4>Axes de Progression</h4>
                    <ul>
                        {#each experience.selfReflection.areasForGrowth as area}
                            <li>{area}</li>
                        {/each}
                    </ul>
                </div>

                <div class="reflection-card full-width">
                    <h4>Manière de Travailler</h4>
                    <p>{experience.selfReflection.workingStyle}</p>
                </div>
            </div>
        </div>
    </div>
</section>

<style>
    .experience-section {
        max-width: 1400px;
        margin: 0 auto;
        padding: 0 20px;
    }

    .experience-container {
        padding: 40px 0;
    }

    .experience-section h1 {
        font-size: 48px;
        text-align: center;
        margin-bottom: 10px;
        background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .subtitle {
        text-align: center;
        color: #94a3b8;
        font-size: 18px;
        margin-bottom: 60px;
    }

    .experience-header {
        background: rgba(30, 41, 59, 0.6);
        border: 1px solid rgba(96, 165, 250, 0.2);
        border-radius: 15px;
        padding: 40px;
        margin-bottom: 60px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        gap: 40px;
    }

    .experience-header h2 {
        font-size: 32px;
        color: #60a5fa;
        margin: 0 0 10px 0;
    }

    .company-context {
        color: #94a3b8;
        margin: 10px 0 20px 0;
        font-size: 15px;
    }

    .meta {
        display: flex;
        gap: 30px;
        flex-wrap: wrap;
    }

    .meta-item {
        color: #cbd5e1;
        font-size: 14px;
    }

    .role-badge {
        display: inline-block;
        background: linear-gradient(135deg, #3b82f6 0%, #8b5cf6 100%);
        color: white;
        padding: 12px 24px;
        border-radius: 25px;
        font-weight: 600;
        white-space: nowrap;
    }

    .main-mission {
        margin-bottom: 80px;
    }

    .main-mission h3 {
        font-size: 28px;
        color: #60a5fa;
        margin-bottom: 30px;
        border-bottom: 2px solid rgba(96, 165, 250, 0.3);
        padding-bottom: 15px;
    }

    .mission-card {
        background: rgba(30, 41, 59, 0.6);
        border: 1px solid rgba(96, 165, 250, 0.2);
        border-radius: 15px;
        padding: 40px;
        border-left: 4px solid #60a5fa;
    }

    .mission-card h4 {
        font-size: 22px;
        color: #e2e8f0;
        margin: 0 0 15px 0;
    }

    .mission-description {
        color: #cbd5e1;
        font-size: 16px;
        margin-bottom: 30px;
        line-height: 1.8;
    }

    .mission-details {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 30px;
        margin-top: 30px;
    }

    .detail-block h5 {
        color: #60a5fa;
        font-size: 14px;
        text-transform: uppercase;
        letter-spacing: 1px;
        margin: 0 0 12px 0;
    }

    .detail-block p {
        color: #94a3b8;
        font-size: 14px;
        line-height: 1.6;
        margin: 0;
    }

    .detail-block ul {
        list-style: none;
        padding: 0;
        margin: 0;
    }

    .detail-block li {
        color: #94a3b8;
        font-size: 14px;
        margin-bottom: 10px;
        padding-left: 20px;
        position: relative;
    }

    .detail-block li::before {
        content: "→";
        position: absolute;
        left: 0;
        color: #60a5fa;
    }

    .team-section {
        background: rgba(30, 41, 59, 0.6);
        border: 1px solid rgba(96, 165, 250, 0.2);
        border-radius: 15px;
        padding: 40px;
        margin-bottom: 80px;
    }

    .team-section h3 {
        font-size: 28px;
        color: #60a5fa;
        margin: 0 0 20px 0;
    }

    .team-text {
        color: #cbd5e1;
        font-size: 15px;
        line-height: 1.8;
        margin: 0;
    }

    .hard-skills-section h3,
    .soft-skills-section h3,
    .reflection-section h3 {
        font-size: 28px;
        color: #60a5fa;
        margin-bottom: 30px;
        border-bottom: 2px solid rgba(96, 165, 250, 0.3);
        padding-bottom: 15px;
    }

    .hard-skills-section {
        margin-bottom: 80px;
    }

    .skills-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 30px;
    }

    .skills-category {
        background: rgba(30, 41, 59, 0.6);
        border: 1px solid rgba(96, 165, 250, 0.2);
        border-radius: 15px;
        padding: 30px;
    }

    .skills-category h4 {
        color: #60a5fa;
        font-size: 18px;
        margin: 0 0 20px 0;
    }

    .skills-list {
        display: flex;
        flex-direction: column;
        gap: 20px;
    }

    .skill-item {
        padding: 15px;
        background: rgba(96, 165, 250, 0.05);
        border-left: 3px solid #60a5fa;
        border-radius: 8px;
    }

    .skill-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 8px;
    }

    .skill-name {
        font-weight: 600;
        color: #e2e8f0;
    }

    .skill-level {
        font-size: 12px;
        color: #60a5fa;
        text-transform: uppercase;
        letter-spacing: 0.5px;
    }

    .skill-context {
        color: #94a3b8;
        font-size: 13px;
        margin: 0;
    }

    .soft-skills-section {
        margin-bottom: 80px;
    }

    .soft-skills-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 30px;
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
    }

    .soft-skill-card h4 {
        color: #60a5fa;
        font-size: 18px;
        margin: 0 0 10px 0;
    }

    .soft-skill-desc {
        color: #94a3b8;
        font-size: 14px;
        margin: 0 0 15px 0;
        font-weight: 500;
    }

    .situation-block {
        background: rgba(96, 165, 250, 0.05);
        border-left: 3px solid #60a5fa;
        padding: 15px;
        border-radius: 8px;
        margin-top: 15px;
    }

    .situation-block p {
        margin: 0 0 8px 0;
        color: #cbd5e1;
        font-size: 13px;
        line-height: 1.6;
    }

    .situation-block p:last-child {
        margin-bottom: 0;
    }

    .reflection-section {
        margin-bottom: 60px;
    }

    .reflection-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 30px;
    }

    .reflection-card {
        background: rgba(30, 41, 59, 0.6);
        border: 1px solid rgba(96, 165, 250, 0.2);
        border-radius: 15px;
        padding: 30px;
    }

    .reflection-card.full-width {
        grid-column: 1 / -1;
    }

    .reflection-card h4 {
        color: #60a5fa;
        font-size: 18px;
        margin: 0 0 20px 0;
    }

    .reflection-card ul {
        list-style: none;
        padding: 0;
        margin: 0;
    }

    .reflection-card li {
        color: #cbd5e1;
        font-size: 14px;
        margin-bottom: 12px;
        padding-left: 20px;
        position: relative;
        line-height: 1.6;
    }

    .reflection-card li::before {
        content: "✓";
        position: absolute;
        left: 0;
        color: #60a5fa;
        font-weight: bold;
    }

    .reflection-card p {
        color: #cbd5e1;
        font-size: 14px;
        line-height: 1.8;
        margin: 0;
    }

    @media (max-width: 768px) {
        .experience-header {
            flex-direction: column;
            align-items: flex-start;
            gap: 20px;
        }

        .meta {
            flex-direction: column;
            gap: 10px;
        }

        .experience-section h1 {
            font-size: 36px;
        }

        .main-mission h3,
        .soft-skills-section h3,
        .hard-skills-section h3,
        .reflection-section h3 {
            font-size: 24px;
        }

        .mission-details {
            grid-template-columns: 1fr;
        }

        .reflection-grid {
            grid-template-columns: 1fr;
        }

        .reflection-card.full-width {
            grid-column: 1;
        }
    }
</style>
