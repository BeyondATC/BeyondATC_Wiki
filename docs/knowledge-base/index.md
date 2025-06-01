---
hide:
  - navigation
  - toc
---

  <style>      
      .container {
            margin: 0 auto;
            padding: 1rem 0rem;
        }
        
        .hero {
            text-align: center;
            margin-bottom: 4rem;
        }
        
        .hero h1 {
            font-size: 3rem;
            font-weight: 700;
            background: linear-gradient(135deg, #6366f1, #8b5cf6, #06b6d4);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            color: #b8c5d1;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .search-bar {
            max-width: 500px;
            margin: 2rem auto;
            position: relative;
        }
        
        .search-input {
            width: 100%;
            padding: 1rem 1.5rem;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 12px;
            color: #fff;
            font-size: 1rem;
            backdrop-filter: blur(10px);
        }
        
        .search-input::placeholder {
            color: #9ca3af;
        }
        
        .search-input:focus {
            outline: none;
            border-color: #6366f1;
            box-shadow: 0 0 0 3px rgba(99, 102, 241, 0.1);
        }
        
        .section {
            margin-bottom: 3rem;
        }
        
        .section-title {
            font-size: 1.8rem;
            font-weight: 600;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 0.75rem;
        }
        
        .section-title .icon {
            width: 2rem;
            height: 2rem;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1rem;
        }
        
        .tutorials .icon {
            background: linear-gradient(135deg, #10b981, #059669);
        }
        
        .info .icon {
            background: linear-gradient(135deg, #3b82f6, #1d4ed8);
        }
        
        .troubleshooting .icon {
            background: linear-gradient(135deg, #f59e0b, #d97706);
        }
        
        .cards-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1rem;
        }
        
        @media (min-width: 1200px) {
            .cards-grid {
                grid-template-columns: repeat(auto-fit, minmax(min(380px, calc((100% - 2rem) / 3)), 1fr));
            }
        }
        
        .card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 12px;
            padding: 1.2rem;
            transition: all 0.3s ease;
            cursor: pointer;
            position: relative;
            overflow: hidden;
            text-decoration: none;
            color: inherit;
            display: block;
        }
        
        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 2px;
            background: linear-gradient(90deg, #6366f1, #8b5cf6);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-3px);
            background: rgba(255, 255, 255, 0.08);
            border-color: rgba(99, 102, 241, 0.3);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
            text-decoration: none;
            color: inherit;
        }
        
        .card:hover::before {
            transform: scaleX(1);
        }
        
        .card-icon {
            width: 2.2rem;
            height: 2.2rem;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            margin-bottom: 0.8rem;
        }
        
        .tutorials .card-icon {
            background: linear-gradient(135deg, #10b981, #059669);
        }
        
        .info .card-icon {
            background: linear-gradient(135deg, #3b82f6, #1d4ed8);
        }
        
        .troubleshooting .card-icon {
            background: linear-gradient(135deg, #f59e0b, #d97706);
        }
        
        .card h3 {
            font-size: 1.1rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
            color: #fff;
            line-height: 1.3;
        }
        
        .card p {
            color: #b8c5d1;
            line-height: 1.4;
            margin-bottom: 1rem;
            font-size: 0.9rem;
            display: -webkit-box;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }
        
        .card-footer {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-top: 1rem;
            padding-top: 0.8rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .difficulty {
            display: flex;
            align-items: center;
            gap: 0.4rem;
            font-size: 0.8rem;
            color: #9ca3af;
        }
        
        .difficulty-dots {
            display: flex;
            gap: 2px;
        }
        
        .dot {
            width: 5px;
            height: 5px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.3);
        }
        
        .dot.active {
            background: #6366f1;
        }
        
        .arrow {
            color: #6366f1;
            font-size: 1rem;
            transition: transform 0.3s ease;
        }
        
        .card:hover .arrow {
            transform: translateX(3px);
        }
        
        .quick-access {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 16px;
            padding: 2rem;
            margin-bottom: 3rem;
        }
        
        .quick-access h2 {
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            color: #fff;
        }
        
        .quick-links {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
        }
        
        .quick-link {
            background: rgba(99, 102, 241, 0.1);
            border: 1px solid rgba(99, 102, 241, 0.2);
            color: #6366f1;
            padding: 0.75rem 1.5rem;
            border-radius: 25px;
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        .quick-link:hover {
            background: rgba(99, 102, 241, 0.2);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(99, 102, 241, 0.2);
        }
        
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
            margin-bottom: 3rem;
        }
        
        .stat-card {
            text-align: center;
            padding: 1.5rem;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .stat-number {
            font-size: 2rem;
            font-weight: 700;
            color: #6366f1;
            margin-bottom: 0.5rem;
        }
        
        .stat-label {
            color: #b8c5d1;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .cards-grid {
                grid-template-columns: 1fr;
            }
            
            .nav {
                display: none;
            }
            
            .container {
                padding: 2rem 1rem;
            }
        }
  </style>

<div class="container">
    <div class="hero">
        <h1>Knowledge Base</h1>
        <p>Find all you need to master BeyondATC. Tutorials, detailed guides and solutions to common problems.</p>
        
        <div class="search-bar">
            <input type="text" class="search-input" placeholder="Search in the knowledge base...">
        </div>
    </div>
    
    <section class="section tutorials">
        <h2 class="section-title">
            <span class="icon">📚</span>
            Tutorials & Guides
        </h2>
        <div class="cards-grid">
            <a href="callsign" class="card" data-title="Setting up your callsign">
                <div class="card-icon">🎯</div>
                <h3>Setting up your callsign</h3>
                <p>This tutorial will help you to use the correct callsign for your flights in Simbrief.</p>
                <div class="card-footer">
                    <div class="difficulty">
                        <span>Easy</span>
                        <div class="difficulty-dots">
                            <span class="dot active"></span>
                            <span class="dot"></span>
                            <span class="dot"></span>
                        </div>
                    </div>
                    <span class="arrow">→</span>
                </div>
            </a>
            
            <a href="msfs2024" class="card" data-title="Getting started with MSFS 2024">
                <div class="card-icon">🚀</div>
                <h3>Getting started with MSFS 2024</h3>
                <p>All information, known issues and guide to get started with MSFS2024 and BeyondATC</p>
                <div class="card-footer">
                    <div class="difficulty">
                        <span>Easy</span>
                        <div class="difficulty-dots">
                            <span class="dot active"></span>
                            <span class="dot"></span>
                            <span class="dot"></span>
                        </div>
                    </div>
                    <span class="arrow">→</span>
                </div>
            </a>
        </div>
    </section>

    <section class="section info">
        <h2 class="section-title">
            <span class="icon">💡</span>
            Useful information
        </h2>
        <div class="cards-grid">
            <a href="atis" class="card" data-title="How ATIS works in BeyondATC">
                <div class="card-icon">🏗️</div>
                <h3>How ATIS works in BeyondATC</h3>
                <p>Discover how BeyondATC builds an ATIS report for every airport and how the information is used to create it.</p>
                <div class="card-footer">
                    <div class="difficulty">
                        <span>Easy</span>
                        <div class="difficulty-dots">
                            <span class="dot active"></span>
                            <span class="dot"></span>
                            <span class="dot"></span>
                        </div>
                    </div>
                    <span class="arrow">→</span>
                </div>
            </a>
            
            <a href="traffic-slider" class="card" data-title="How the traffic sliders work">
                <div class="card-icon">🚦</div>
                <h3>How the traffic sliders work</h3>
                <p>Understand how traffic sliders influence the density and realism of your flying environment.</p>
                <div class="card-footer">
                    <div class="difficulty">
                        <span>Intermediate</span>
                        <div class="difficulty-dots">
                            <span class="dot active"></span>
                            <span class="dot active"></span>
                            <span class="dot"></span>
                        </div>
                    </div>
                    <span class="arrow">→</span>
                </div>
            </a>
            
            <a href="airport-sop" class="card" data-title="Airport SOPs implementation">
                <div class="card-icon">✈️</div>
                <h3>Airport SOPs implementation</h3>
                <p>Detailed guide to implementing SOPs (Standard Operating Procedures) in BeyondATC.</p>
                <div class="card-footer">
                    <div class="difficulty">
                        <span>Advanced</span>
                        <div class="difficulty-dots">
                            <span class="dot active"></span>
                            <span class="dot active"></span>
                            <span class="dot active"></span>
                        </div>
                    </div>
                    <span class="arrow">→</span>
                </div>
            </a>
            
            <a href="squawk-1000" class="card" data-title="Squawk 1000 in Europe">
                <div class="card-icon">📻</div>
                <h3>Squawk 1000 in Europe</h3>
                <p>Find out all about the use of transponder code 1000 in European airspace and its implications.</p>
                <div class="card-footer">
                    <div class="difficulty">
                        <span>Easy</span>
                        <div class="difficulty-dots">
                            <span class="dot active"></span>
                            <span class="dot"></span>
                            <span class="dot"></span>
                        </div>
                    </div>
                    <span class="arrow">→</span>
                </div>
            </a>
        </div>
    </section>

    <section class="section troubleshooting">
        <h2 class="section-title">
            <span class="icon">🔧</span>
            Troubleshooting & Support
        </h2>
        <div class="cards-grid">
            <a href="core-engine" class="card" data-title="Change the BeyondATC Core Engine">
                <div class="card-icon">⚙️</div>
                <h3>Change the BeyondATC Core Engine</h3>
                <p>Instructions for changing the core engine to suit your specific needs in case you have problems running BeyondATC.</p>
                <div class="card-footer">
                    <div class="difficulty">
                        <span>Easy</span>
                        <div class="difficulty-dots">
                            <span class="dot active"></span>
                            <span class="dot"></span>
                            <span class="dot"></span>
                        </div>
                    </div>
                    <span class="arrow">→</span>
                </div>
            </a>
            
            <a href="../support/common-issues/simconnect" class="card" data-title="Troubleshoot connection issues">
                <div class="card-icon">🔌</div>
                <h3>Troubleshoot connection issues</h3>
                <p>Solutions to the most common connection problems between BeyondATC and your simulator.</p>
                <div class="card-footer">
                    <div class="difficulty">
                        <span>Easy</span>
                        <div class="difficulty-dots">
                            <span class="dot active"></span>
                            <span class="dot"></span>
                            <span class="dot"></span>
                        </div>
                    </div>
                    <span class="arrow">→</span>
                </div>
            </a>
        </div>
    </section>
</div>

<script>
  function initCardScripts() {
    // Animation d'entrée des cartes
    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.style.opacity = '1';
          entry.target.style.transform = 'translateY(0)';
        }
      });
    });

    const cards = document.querySelectorAll('.card');

    cards.forEach((card, index) => {
      card.style.opacity = '0';
      card.style.transform = 'translateY(20px)';
      card.style.transition = `all 0.6s ease ${index * 0.1}s`;
      observer.observe(card);
    });

    // Recherche en temps réel
    const searchInput = document.querySelector('.search-input');
    if (searchInput) {
      searchInput.addEventListener('input', (e) => {
        const searchTerm = e.target.value.toLowerCase();

        cards.forEach(card => {
          const title = card.querySelector('h3').textContent.toLowerCase();
          const description = card.querySelector('p').textContent.toLowerCase();

          if (title.includes(searchTerm) || description.includes(searchTerm)) {
            card.style.display = 'block';
            card.style.animation = 'fadeIn 0.3s ease';
          } else {
            card.style.display = searchTerm === '' ? 'block' : 'none';
          }
        });
      });
    }
  }

  // Compatibilité avec MkDocs Material (navigation instantanée)
  document.addEventListener("DOMContentLoaded", initCardScripts);
  document.addEventListener("pjax:content", initCardScripts);
</script>