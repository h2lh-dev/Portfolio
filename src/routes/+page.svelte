<script>
    import { onMount } from "svelte";

    let scrollY = 0;

    onMount(() => {
        window.addEventListener("scroll", () => {
            scrollY = window.scrollY;
        });
    });
</script>

<svelte:window bind:scrollY/>

<section class="hero">
    <div class="hero-content">
        <div class="hero-text">
            <h1 class="hero-title">Hugo Desmons</h1>
            <p class="hero-subtitle">Développeur Full Stack</p>
            <p class="hero-tagline">Passionné par la création d'expériences digitales | Backend & Frontend | Web & Mobile</p>
            <p class="hero-description">Développeur Full Stack avec expérience professionnelle en contexte international. Spécialisé dans la création d'applications web modernes utilisant Laravel, React et technologies cloud. Doté de capacités d'adaptation rapide et d'autonomie dans la gestion de projets complets.</p>
            <div class="hero-cta">
                <a href="/Experience" class="btn btn-primary">Mon expérience</a>
                <a href="/Projet" class="btn btn-secondary">Voir mes projets</a>
            </div>
        </div>
    </div>
</section>

<section class="positioning">
    <div class="positioning-container">
        <h2>Qui suis-je professionnellement ?</h2>
        <div class="positioning-grid">
            <div class="positioning-card">
                <div class="card-number">01</div>
                <h3>Profil</h3>
                <p>Développeur Full Stack en formation BUT Informatique (3ème année). Expérience de 3 mois en tant que développeur chez AnankéInc au Canada en contexte Erasmus.</p>
            </div>
            <div class="positioning-card">
                <div class="card-number">02</div>
                <h3>Compétences clés</h3>
                <p>PHP/Laravel, JavaScript/Tailwind, Gestion de base de données, Architecture logicielle, Méthodologies Agile, Travail en équipe distribuée.</p>
            </div>
            <div class="positioning-card">
                <div class="card-number">03</div>
                <h3>Points forts</h3>
                <p>Autonomie, adaptabilité, apprentissage rapide, communication efficace, capacité à prendre l'initiative dans un environnement peu structuré.</p>
            </div>
            <div class="positioning-card">
                <div class="card-number">04</div>
                <h3>Projet</h3>
                <p>Rejoindre une équipe en tant que développeur Full Stack ou spécialiser progressivement mes compétences (Backend ou DevOps).</p>
            </div>
        </div>
    </div>
</section>

<section class="highlights">
    <div class="highlights-container">
        <h2>Points forts</h2>
        <div class="highlights-grid">
            <div class="highlight-item">
                <div class="highlight-icon">🚀</div>
                <h3>Semi-autonomie</h3>
                <p>Capable de gérer un projet complet de bout en bout avec respect des directives et livrables définis.</p>
            </div>
            <div class="highlight-item">
                <div class="highlight-icon">🌍</div>
                <h3>Adaptabilité</h3>
                <p>Expérience en contexte international (stage Erasmus), capacité à s'adapter rapidement à un nouvel environnement professionnel.</p>
            </div>
            <div class="highlight-item">
                <div class="highlight-icon">💡</div>
                <h3>Apprentissage rapide</h3>
                <p>Technologies maîtrisées en situation réelle dans un contexte professionnel sans formation préalable intensive.</p>
            </div>
            <div class="highlight-item">
                <div class="highlight-icon">👥</div>
                <h3>Collaboration</h3>
                <p>Travail efficace dans une petite équipe (3 personnes) avec communication régulière et responsabilité partagée.</p>
            </div>
        </div>
    </div>
</section>

<section class="cta-section">
    <div class="cta-content">
        <h2>Découvrez mon parcours complet</h2>
        <p>Explorez mon expérience professionnelle, mes compétences et mes projets significatifs</p>
        <div class="cta-buttons">
            <a href="/Experience" class="btn btn-primary">Expérience & Compétences</a>
            <a href="/Competence" class="btn btn-secondary">Soft Skills</a>
        </div>
    </div>
</section>

<style>
    .hero {
        margin: -60px -20px 100px;
        padding: 100px 20px;
        background: linear-gradient(135deg, rgba(59, 130, 246, 0.1) 0%, rgba(139, 92, 246, 0.1) 100%);
        border-bottom: 1px solid rgba(96, 165, 250, 0.2);
    }

    .hero-content {
        max-width: 1400px;
        margin: 0 auto;
        display: grid;
        grid-template-columns: 1fr;
        gap: 60px;
    }

    .hero-text {
        z-index: 2;
    }

    .hero-title {
        font-size: 56px;
        font-weight: 800;
        background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
        margin-bottom: 10px;
        line-height: 1.2;
    }

    .hero-subtitle {
        font-size: 28px;
        font-weight: 300;
        color: #cbd5e1;
        margin-bottom: 10px;
    }

    .hero-tagline {
        font-size: 16px;
        color: #60a5fa;
        font-weight: 500;
        margin-bottom: 20px;
        text-transform: uppercase;
        letter-spacing: 1px;
    }

    .hero-description {
        font-size: 16px;
        color: #94a3b8;
        margin-bottom: 40px;
        line-height: 1.8;
        max-width: 700px;
    }

    .hero-cta {
        display: flex;
        gap: 20px;
        flex-wrap: wrap;
    }

    .btn {
        display: inline-block;
        padding: 14px 32px;
        border-radius: 10px;
        font-weight: 600;
        font-size: 15px;
        transition: all 0.3s ease;
        border: 2px solid transparent;
        cursor: pointer;
        text-decoration: none;
        text-align: center;
    }

    .btn-primary {
        background: linear-gradient(135deg, #3b82f6 0%, #8b5cf6 100%);
        color: white;
        box-shadow: 0 4px 20px rgba(59, 130, 246, 0.3);
    }

    .btn-primary:hover {
        transform: translateY(-2px);
        box-shadow: 0 8px 30px rgba(59, 130, 246, 0.5);
    }

    .btn-secondary {
        background: transparent;
        color: #60a5fa;
        border: 2px solid #60a5fa;
    }

    .btn-secondary:hover {
        background: rgba(96, 165, 250, 0.1);
        border-color: #93c5fd;
        color: #93c5fd;
    }

    .positioning {
        margin: 100px 0;
    }

    .positioning-container {
        max-width: 1400px;
        margin: 0 auto;
        padding: 0 20px;
    }

    .positioning-container h2 {
        font-size: 40px;
        text-align: center;
        margin-bottom: 60px;
        background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .positioning-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 30px;
    }

    .positioning-card {
        background: rgba(30, 41, 59, 0.6);
        border: 1px solid rgba(96, 165, 250, 0.2);
        border-radius: 15px;
        padding: 40px 30px;
        transition: all 0.3s ease;
        position: relative;
    }

    .positioning-card:hover {
        border-color: rgba(96, 165, 250, 0.5);
        box-shadow: 0 10px 40px rgba(59, 130, 246, 0.1);
        transform: translateY(-5px);
    }

    .card-number {
        font-size: 48px;
        font-weight: 800;
        color: rgba(96, 165, 250, 0.2);
        position: absolute;
        top: 20px;
        right: 30px;
    }

    .positioning-card h3 {
        font-size: 22px;
        color: #60a5fa;
        margin-bottom: 15px;
        margin-top: 0;
    }

    .positioning-card p {
        color: #94a3b8;
        line-height: 1.8;
        font-size: 15px;
        margin: 0;
    }

    .highlights {
        margin: 100px 0;
    }

    .highlights-container {
        max-width: 1400px;
        margin: 0 auto;
        padding: 0 20px;
    }

    .highlights-container h2 {
        font-size: 40px;
        text-align: center;
        margin-bottom: 60px;
        background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .highlights-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 30px;
    }

    .highlight-item {
        background: rgba(30, 41, 59, 0.6);
        border: 1px solid rgba(96, 165, 250, 0.2);
        border-radius: 15px;
        padding: 40px 30px;
        text-align: center;
        transition: all 0.3s ease;
    }

    .highlight-item:hover {
        border-color: rgba(96, 165, 250, 0.5);
        box-shadow: 0 10px 40px rgba(59, 130, 246, 0.1);
        transform: translateY(-5px);
    }

    .highlight-icon {
        font-size: 40px;
        margin-bottom: 15px;
    }

    .highlight-item h3 {
        font-size: 20px;
        color: #60a5fa;
        margin-bottom: 12px;
    }

    .highlight-item p {
        color: #94a3b8;
        font-size: 15px;
        line-height: 1.6;
        margin: 0;
    }

    .cta-section {
        background: linear-gradient(135deg, rgba(59, 130, 246, 0.1) 0%, rgba(139, 92, 246, 0.1) 100%);
        border: 1px solid rgba(96, 165, 250, 0.2);
        border-radius: 20px;
        padding: 80px 40px;
        text-align: center;
        margin: 100px 20px;
    }

    .cta-content h2 {
        font-size: 42px;
        margin-bottom: 20px;
        background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .cta-content p {
        font-size: 18px;
        color: #94a3b8;
        margin-bottom: 40px;
    }

    .cta-buttons {
        display: flex;
        gap: 20px;
        justify-content: center;
        flex-wrap: wrap;
    }

    @media (max-width: 768px) {
        .hero-title {
            font-size: 42px;
        }

        .hero-subtitle {
            font-size: 20px;
        }

        .positioning-container h2 {
            font-size: 32px;
        }

        .highlights-container h2 {
            font-size: 32px;
        }

        .cta-section {
            padding: 50px 20px;
        }

        .cta-content h2 {
            font-size: 32px;
        }

        .hero-cta {
            flex-direction: column;
        }

        .btn {
            width: 100%;
        }
    }
</style>

