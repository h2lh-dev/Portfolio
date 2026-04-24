<footer>
    <div class="footer-content">
        <div class="footer-section">
            <h3>Hugo Desmons</h3>
            <p>Étudiant BUT Informatique - Développeur Full Stack</p>
        </div>

        <div class="footer-section">
            <h4>Navigation</h4>
            <ul>
                <li><a href="/">Accueil</a></li>
                <li><a href="/Projet">Projets</a></li>
                <li><a href="/Parcours">Parcours</a></li>
                <li><a href="/Competence">Compétences</a></li>
            </ul>
        </div>

        <div class="footer-section">
            <h4>Liens</h4>
            <ul>
                <li><a href="https://github.com/h2lh-dev" target="_blank">GitHub</a></li>
                <li><a href="https://www.linkedin.com/in/hugo-desmons-a65b31313" target="_blank">LinkedIn</a></li>
                <li><a href="./Projet/CVHugoDesmons.pdf" download>CV</a></li>
            </ul>
        </div>

        <div class="footer-section">
            <h4>Contact</h4>
            <p><a href="mailto:hugo.desmons@icloud.com">hugo.desmons@icloud.com</a></p>
        </div>
    </div>

    <div class="footer-bottom">
        <p>&copy; 2025 Hugo Desmons. Tous droits réservés.</p>
    </div>
</footer>

<style>
    footer {
        background: linear-gradient(135deg, rgba(15, 23, 42, 0.95) 0%, rgba(30, 41, 59, 0.95) 100%);
        border-top: 1px solid rgba(96, 165, 250, 0.2);
        color: #cbd5e1;
        padding: 60px 20px 30px;
        margin-top: 100px;
    }

    .footer-content {
        max-width: 1400px;
        margin: 0 auto 40px;
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 40px;
    }

    .footer-section h3 {
        font-size: 20px;
        margin-bottom: 10px;
        background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .footer-section h4 {
        font-size: 14px;
        font-weight: 600;
        color: #60a5fa;
        margin-bottom: 15px;
        text-transform: uppercase;
        letter-spacing: 1px;
    }

    .footer-section p {
        font-size: 14px;
        color: #94a3b8;
        line-height: 1.8;
    }

    .footer-section ul {
        list-style: none;
    }

    .footer-section ul li {
        margin-bottom: 8px;
    }

    .footer-section a {
        color: #94a3b8;
        font-size: 14px;
        transition: all 0.3s ease;
    }

    .footer-section a:hover {
        color: #60a5fa;
        transform: translateX(4px);
    }

    .footer-bottom {
        max-width: 1400px;
        margin: 0 auto;
        padding-top: 30px;
        border-top: 1px solid rgba(96, 165, 250, 0.1);
        text-align: center;
        color: #64748b;
        font-size: 13px;
    }

    @media (max-width: 768px) {
        footer {
            padding: 40px 20px 20px;
        }

        .footer-content {
            gap: 30px;
        }

        .footer-section h3 {
            font-size: 18px;
        }
    }
</style>