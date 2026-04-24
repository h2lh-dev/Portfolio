<script>
    const timeline = [
        {
            date: "Avril 2025 - Juin 2025",
            title: "Stage AnankéInc",
            description: "Stage Erasmus au Canada",
            side: "left",
            icon: "🌍"
        },
        {
            date: "2022 - 2026",
            title: "BUT Informatique",
            description: "IUT A Villeneuve d'Ascq - Université de Lille",
            side: "right",
            icon: "🎓"
        },
        {
            date: "2019 - 2022",
            title: "Baccalauréat STI2D",
            description: "Sciences et technologies de l'industrie et du développement durable - Lycées Edmond Labbé (Douai)",
            side: "left",
            icon: "📚"
        }
    ];
</script>

<section class="parcours-section">
    <div class="parcours-header">
        <h1>Mon Parcours</h1>
        <p>Découvrez mon évolution académique et professionnelle</p>
    </div>

    <div class="timeline">
        {#each timeline as event, index (event.title)}
            <div class="timeline-item {event.side}">
                <div class="timeline-marker">
                    <div class="marker-dot"></div>
                    {#if index !== timeline.length - 1}
                        <div class="marker-line"></div>
                    {/if}
                </div>
                <div class="timeline-content">
                    <div class="timeline-card">
                        <div class="card-icon">{event.icon}</div>
                        <div class="card-text">
                            <time class="card-date">{event.date}</time>
                            <h3 class="card-title">{event.title}</h3>
                            <p class="card-description">{event.description}</p>
                        </div>
                    </div>
                </div>
            </div>
        {/each}
    </div>
</section>

<style>
    .parcours-section {
        max-width: 1000px;
        margin: 0 auto;
        padding: 0 20px;
    }

    .parcours-header {
        text-align: center;
        margin-bottom: 80px;
    }

    .parcours-header h1 {
        font-size: 48px;
        margin-bottom: 20px;
        background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .parcours-header p {
        font-size: 18px;
        color: #94a3b8;
    }

    .timeline {
        position: relative;
        padding: 40px 0;
    }

    .timeline::before {
        content: '';
        position: absolute;
        left: 50%;
        top: 0;
        bottom: 0;
        width: 2px;
        background: linear-gradient(180deg, rgba(96, 165, 250, 0.3) 0%, rgba(139, 92, 246, 0.3) 50%, rgba(96, 165, 250, 0.3) 100%);
        transform: translateX(-50%);
    }

    .timeline-item {
        position: relative;
        margin-bottom: 50px;
        display: flex;
    }

    .timeline-item.left {
        justify-content: flex-start;
    }

    .timeline-item.right {
        justify-content: flex-end;
    }

    .timeline-marker {
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        z-index: 10;
        display: flex;
        flex-direction: column;
        align-items: center;
        top: 0;
    }

    .marker-dot {
        width: 20px;
        height: 20px;
        background: linear-gradient(135deg, #3b82f6 0%, #8b5cf6 100%);
        border: 4px solid rgba(15, 23, 42, 1);
        border-radius: 50%;
        box-shadow: 0 0 0 3px rgba(96, 165, 250, 0.3);
    }

    .marker-line {
        width: 2px;
        height: 40px;
        background: linear-gradient(180deg, rgba(96, 165, 250, 0.2) 0%, rgba(96, 165, 250, 0) 100%);
    }

    .timeline-content {
        width: 45%;
    }

    .timeline-item.left .timeline-content {
        text-align: right;
        padding-right: 50px;
    }

    .timeline-item.right .timeline-content {
        text-align: left;
        padding-left: 50px;
    }

    .timeline-card {
        background: rgba(30, 41, 59, 0.6);
        border: 1px solid rgba(96, 165, 250, 0.2);
        border-radius: 15px;
        padding: 30px;
        transition: all 0.3s ease;
        display: flex;
        gap: 20px;
        align-items: flex-start;
    }

    .timeline-card:hover {
        border-color: rgba(96, 165, 250, 0.5);
        box-shadow: 0 15px 40px rgba(59, 130, 246, 0.15);
        transform: translateY(-5px);
        background: rgba(30, 41, 59, 0.8);
    }

    .card-icon {
        font-size: 32px;
        flex-shrink: 0;
        min-width: 50px;
        text-align: center;
    }

    .card-text {
        flex: 1;
    }

    .card-date {
        display: block;
        font-size: 14px;
        color: #60a5fa;
        font-weight: 600;
        margin-bottom: 8px;
        text-transform: uppercase;
        letter-spacing: 1px;
    }

    .card-title {
        font-size: 22px;
        color: #e2e8f0;
        margin: 8px 0;
        font-weight: 700;
    }

    .card-description {
        font-size: 15px;
        color: #94a3b8;
        line-height: 1.6;
        margin: 0;
    }

    @media (max-width: 768px) {
        .timeline::before {
            left: 30px;
        }

        .timeline-item {
            margin-bottom: 40px;
            justify-content: flex-start !important;
        }

        .timeline-marker {
            left: 30px;
        }

        .timeline-content {
            width: calc(100% - 100px) !important;
            text-align: left !important;
            padding: 0 0 0 50px !important;
        }

        .timeline-card {
            flex-direction: column;
        }

        .card-icon {
            text-align: left;
        }

        .parcours-header h1 {
            font-size: 36px;
        }
    }
</style>