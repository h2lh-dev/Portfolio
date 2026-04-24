<script>
    import { onMount } from ‘svelte’;

    let scrollY = 0;

    onMount(() => {
        window.addEventListener(‘scroll’, () => {
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
            <p class="hero-description">Étudiant en BUT Informatique à l’IUT de Villeneuve d’Ascq, passionné par les technologies numériques et l’innovation</p>
            <div class="hero-cta">
                <a href="/Projet" class="btn btn-primary">Voir mes projets</a>
                <a href="./Projet/CVHugoDesmons.pdf" download class="btn btn-secondary">Télécharger CV</a>
            </div>
        </div>
        <div class="hero-visual" style="transform: translateY({scrollY * 0.5}px)">
            <div class="gradient-box gradient-1"></div>
            <div class="gradient-box gradient-2"></div>
            <div class="gradient-box gradient-3"></div>
        </div>
    </div>
</section>

<section class="presentation">
    <div class="presentation-container">
        <h2>À propos de moi</h2>
        <div class="presentation-grid">
            <div class="presentation-card">
                <div class="card-icon">📚</div>
                <h3>Formation</h3>
                <p>Actuellement en 2ème année de BUT Informatique à l’IUT de Villeneuve d’Ascq. Passionné par les technologies numériques et le développement logiciel.</p>
            </div>
            <div class="presentation-card">
                <div class="card-icon">💡</div>
                <h3>Vision</h3>
                <p>Convaincu que les intelligences artificielles et les innovations constantes offrent des perspectives d’avenir passionnantes et stimulantes.</p>
            </div>
            <div class="presentation-card">
                <div class="card-icon">🚀</div>
                <h3>Objectifs</h3>
                <p>Poursuivre ma formation en alternance et développer mes compétences dans le domaine du développement logiciel riche et diversifié.</p>
            </div>
        </div>
    </div>
</section>

<section class="cta-section">
    <div class="cta-content">
        <h2>Prêt à collaborer ?</h2>
        <p>Explorez mes projets et découvrez comment je peux contribuer à vos ambitions</p>
        <div class="cta-buttons">
            <a href="/Projet" class="btn btn-primary">Consulter les projets</a>
            <a href="mailto:hugo.desmons@icloud.com" class="btn btn-secondary">Me contacter</a>
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
        grid-template-columns: 1fr 1fr;
        gap: 60px;
        align-items: center;
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
        margin-bottom: 20px;
    }

    .hero-description {
        font-size: 16px;
        color: #94a3b8;
        margin-bottom: 40px;
        line-height: 1.8;
        max-width: 500px;
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

    .hero-visual {
        position: relative;
        height: 300px;
        display: none;
    }

    .gradient-box {
        position: absolute;
        border-radius: 20px;
        filter: blur(40px);
        opacity: 0.6;
    }

    .gradient-1 {
        width: 200px;
        height: 200px;
        background: linear-gradient(135deg, #3b82f6, #8b5cf6);
        top: 0;
        right: 0;
        animation: float 6s ease-in-out infinite;
    }

    .gradient-2 {
        width: 150px;
        height: 150px;
        background: linear-gradient(135deg, #8b5cf6, #ec4899);
        bottom: 50px;
        left: 50px;
        animation: float 8s ease-in-out infinite reverse;
    }

    .gradient-3 {
        width: 180px;
        height: 180px;
        background: linear-gradient(135deg, #06b6d4, #3b82f6);
        top: 150px;
        left: 100px;
        animation: float 7s ease-in-out infinite;
    }

    @keyframes float {
        0%, 100% { transform: translateY(0px); }
        50% { transform: translateY(20px); }
    }

    .presentation {
        margin: 100px 0;
    }

    .presentation-container {
        max-width: 1400px;
        margin: 0 auto;
        padding: 0 20px;
    }

    .presentation-container h2 {
        font-size: 40px;
        text-align: center;
        margin-bottom: 60px;
        background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .presentation-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 30px;
    }

    .presentation-card {
        background: rgba(30, 41, 59, 0.6);
        border: 1px solid rgba(96, 165, 250, 0.2);
        border-radius: 15px;
        padding: 40px 30px;
        transition: all 0.3s ease;
    }

    .presentation-card:hover {
        border-color: rgba(96, 165, 250, 0.5);
        box-shadow: 0 10px 40px rgba(59, 130, 246, 0.1);
        transform: translateY(-5px);
    }

    .card-icon {
        font-size: 40px;
        margin-bottom: 20px;
    }

    .presentation-card h3 {
        font-size: 22px;
        color: #60a5fa;
        margin-bottom: 15px;
    }

    .presentation-card p {
        color: #94a3b8;
        line-height: 1.8;
        font-size: 15px;
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
        .hero-content {
            grid-template-columns: 1fr;
        }

        .hero-title {
            font-size: 42px;
        }

        .hero-subtitle {
            font-size: 20px;
        }

        .presentation-container h2 {
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