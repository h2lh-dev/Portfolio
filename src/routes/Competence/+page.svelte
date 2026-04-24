<script>
    const competences = [
        {
            category: "Frontend",
            skills: [
                { name: "HTML", icon: "html", level: 90 },
                { name: "CSS", icon: "css", level: 85 },
                { name: "JavaScript", icon: "javascript", level: 80 },
                { name: "Svelte", icon: "svelte", level: 75 }
            ]
        },
        {
            category: "Backend",
            skills: [
                { name: "Java", icon: "java", level: 85 },
                { name: "PostgreSQL", icon: "postgresql", level: 80 },
                { name: "Linux", icon: "linux", level: 75 }
            ]
        },
        {
            category: "Outils & Design",
            skills: [
                { name: "Git", icon: "git", level: 85 },
                { name: "Figma", icon: "figma", level: 75 },
                { name: "Genially", icon: "genially", level: 70 },
                { name: "JetBrains", icon: "idea", level: 80 }
            ]
        },
        {
            category: "Autres",
            skills: [
                { name: "C", icon: "c", level: 70 },
                { name: "VirtualBox", icon: "virtualbox", level: 75 }
            ]
        }
    ];
</script>

<section class="competences-section">
    <div class="competences-header">
        <h1>Mes Compétences</h1>
        <p>Ensemble des technologies et outils que j'ai maîtrisés durant ma formation</p>
    </div>

    <div class="competences-container">
        {#each competences as category (category.category)}
            <div class="category-section">
                <h2 class="category-title">{category.category}</h2>
                <div class="skills-grid">
                    {#each category.skills as skill (skill.name)}
                        <div class="skill-card">
                            <div class="skill-icon">
                                {#if skill.icon === "html"}
                                    <img src="https://skillicons.dev/icons?i=html&theme=light" alt={skill.name} />
                                {:else if skill.icon === "css"}
                                    <img src="https://skillicons.dev/icons?i=css&theme=light" alt={skill.name} />
                                {:else if skill.icon === "javascript"}
                                    <img src="https://skillicons.dev/icons?i=javascript&theme=light" alt={skill.name} />
                                {:else if skill.icon === "svelte"}
                                    <img src="https://skillicons.dev/icons?i=svelte&theme=light" alt={skill.name} />
                                {:else if skill.icon === "java"}
                                    <img src="https://skillicons.dev/icons?i=java&theme=light" alt={skill.name} />
                                {:else if skill.icon === "postgresql"}
                                    <img src="https://skillicons.dev/icons?i=postgresql&theme=light" alt={skill.name} />
                                {:else if skill.icon === "linux"}
                                    <img src="https://skillicons.dev/icons?i=linux&theme=light" alt={skill.name} />
                                {:else if skill.icon === "git"}
                                    <img src="https://skillicons.dev/icons?i=git&theme=light" alt={skill.name} />
                                {:else if skill.icon === "figma"}
                                    <img src="https://skillicons.dev/icons?i=figma&theme=light" alt={skill.name} />
                                {:else if skill.icon === "c"}
                                    <img src="https://skillicons.dev/icons?i=c&theme=light" alt={skill.name} />
                                {:else if skill.icon === "idea"}
                                    <img src="https://skillicons.dev/icons?i=idea&theme=light" alt={skill.name} />
                                {:else}
                                    <div class="icon-placeholder">{skill.name.charAt(0)}</div>
                                {/if}
                            </div>
                            <h3>{skill.name}</h3>
                            <div class="progress-bar">
                                <div class="progress-fill" style="width: {skill.level}%"></div>
                            </div>
                            <span class="level">{skill.level}%</span>
                        </div>
                    {/each}
                </div>
            </div>
        {/each}
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
        display: grid;
        gap: 60px;
    }

    .category-section {
        margin-bottom: 40px;
    }

    .category-title {
        font-size: 32px;
        margin-bottom: 40px;
        color: #60a5fa;
        position: relative;
        padding-bottom: 15px;
    }

    .category-title::after {
        content: '';
        position: absolute;
        bottom: 0;
        left: 0;
        width: 60px;
        height: 3px;
        background: linear-gradient(90deg, #3b82f6, #8b5cf6);
        border-radius: 2px;
    }

    .skills-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
        gap: 25px;
    }

    .skill-card {
        background: rgba(30, 41, 59, 0.6);
        border: 1px solid rgba(96, 165, 250, 0.2);
        border-radius: 15px;
        padding: 30px 20px;
        text-align: center;
        transition: all 0.3s ease;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .skill-card:hover {
        border-color: rgba(96, 165, 250, 0.5);
        box-shadow: 0 15px 40px rgba(59, 130, 246, 0.15);
        transform: translateY(-8px);
        background: rgba(30, 41, 59, 0.8);
    }

    .skill-icon {
        width: 70px;
        height: 70px;
        margin-bottom: 15px;
        display: flex;
        align-items: center;
        justify-content: center;
        background: rgba(59, 130, 246, 0.1);
        border-radius: 12px;
        transition: all 0.3s ease;
    }

    .skill-card:hover .skill-icon {
        background: rgba(59, 130, 246, 0.2);
        transform: scale(1.05);
    }

    .skill-icon img {
        width: 50px;
        height: 50px;
        object-fit: contain;
    }

    .icon-placeholder {
        font-size: 32px;
        font-weight: 700;
        color: #60a5fa;
    }

    .skill-card h3 {
        font-size: 18px;
        color: #60a5fa;
        margin-bottom: 15px;
        font-weight: 600;
    }

    .progress-bar {
        width: 100%;
        height: 6px;
        background: rgba(96, 165, 250, 0.1);
        border-radius: 3px;
        overflow: hidden;
        margin-bottom: 10px;
    }

    .progress-fill {
        height: 100%;
        background: linear-gradient(90deg, #3b82f6, #8b5cf6);
        border-radius: 3px;
        transition: width 0.6s ease;
    }

    .level {
        font-size: 12px;
        color: #94a3b8;
        font-weight: 500;
    }

    @media (max-width: 768px) {
        .competences-header h1 {
            font-size: 36px;
        }

        .category-title {
            font-size: 24px;
        }

        .skills-grid {
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 20px;
        }

        .skill-card {
            padding: 20px 15px;
        }

        .skill-icon {
            width: 60px;
            height: 60px;
        }

        .skill-icon img {
            width: 40px;
            height: 40px;
        }
    }
</style>