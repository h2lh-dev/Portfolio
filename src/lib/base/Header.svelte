<script>
    let isOpen = false;

    function toggleMenu() {
        isOpen = !isOpen;
    }

    function closeMenu() {
        isOpen = false;
    }
</script>

<header>
    <nav class="navbar">
        <div class="nav-container">
            <div class="logo">
                <a href="/" on:click={closeMenu}>
                    <span class="logo-text">HD</span>
                </a>
            </div>

            <button class="menu-toggle" on:click={toggleMenu} aria-label="Toggle menu">
                <span class:active={isOpen}></span>
                <span class:active={isOpen}></span>
                <span class:active={isOpen}></span>
            </button>

            <ul class="nav-menu" class:active={isOpen}>
                <li><a href="/" on:click={closeMenu}>Accueil</a></li>
                <li><a href="/Experience" on:click={closeMenu}>Expérience</a></li>
                <li><a href="/Projet" on:click={closeMenu}>Projets</a></li>
                <li><a href="/Parcours" on:click={closeMenu}>Parcours</a></li>
                <li><a href="/Competence" on:click={closeMenu}>Compétences</a></li>
            </ul>
        </div>
    </nav>
</header>

<style>
    header {
        position: sticky;
        top: 0;
        z-index: 1000;
        background: rgba(15, 23, 42, 0.95);
        backdrop-filter: blur(10px);
        border-bottom: 1px solid rgba(96, 165, 250, 0.2);
    }

    .navbar {
        padding: 0;
    }

    .nav-container {
        max-width: 1400px;
        margin: 0 auto;
        padding: 15px 20px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .logo {
        display: flex;
        align-items: center;
    }

    .logo a {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 45px;
        height: 45px;
        background: linear-gradient(135deg, #3b82f6 0%, #8b5cf6 100%);
        border-radius: 10px;
        font-weight: 700;
        font-size: 18px;
        color: white;
        transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .logo a:hover {
        transform: translateY(-2px);
        box-shadow: 0 8px 20px rgba(59, 130, 246, 0.4);
    }

    .logo-text {
        color: white;
    }

    .nav-menu {
        display: flex;
        list-style: none;
        gap: 40px;
        align-items: center;
    }

    .nav-menu li a {
        color: #cbd5e1;
        font-size: 15px;
        font-weight: 500;
        transition: all 0.3s ease;
        position: relative;
    }

    .nav-menu li a::after {
        content: "";
        position: absolute;
        bottom: -5px;
        left: 0;
        width: 0;
        height: 2px;
        background: linear-gradient(90deg, #3b82f6, #8b5cf6);
        transition: width 0.3s ease;
    }

    .nav-menu li a:hover {
        color: #60a5fa;
    }

    .nav-menu li a:hover::after {
        width: 100%;
    }

    .menu-toggle {
        display: none;
        flex-direction: column;
        background: none;
        border: none;
        cursor: pointer;
        padding: 0;
        gap: 6px;
    }

    .menu-toggle span {
        width: 25px;
        height: 3px;
        background: #60a5fa;
        border-radius: 2px;
        transition: all 0.3s ease;
    }

    .menu-toggle span.active:nth-child(1) {
        transform: rotate(45deg) translate(8px, 8px);
    }

    .menu-toggle span.active:nth-child(2) {
        opacity: 0;
    }

    .menu-toggle span.active:nth-child(3) {
        transform: rotate(-45deg) translate(8px, -8px);
    }

    @media (max-width: 768px) {
        .menu-toggle {
            display: flex;
        }

        .nav-menu {
            position: absolute;
            top: 70px;
            left: 0;
            width: 100%;
            flex-direction: column;
            background: rgba(15, 23, 42, 0.98);
            gap: 0;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease;
        }

        .nav-menu.active {
            max-height: 300px;
        }

        .nav-menu li {
            width: 100%;
            border-bottom: 1px solid rgba(96, 165, 250, 0.1);
        }

        .nav-menu li a {
            display: block;
            padding: 15px 20px;
            color: #cbd5e1;
        }

        .nav-menu li a::after {
            display: none;
        }

        .nav-menu li a:hover {
            background: rgba(59, 130, 246, 0.1);
            color: #60a5fa;
        }
    }
</style>
