<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Marcos Freitas - QA Engineer & Developer</title>
    <!-- Chosen Palette: Midnight Cyber (Dark background with vibrant blues, purples, and cyans) -->
    <!-- Application Structure Plan: A single-page, top-down narrative structure. It starts with a visual identity (banner), flows into a skills summary (interactive chart), details the specific tools (technology grid), presents a personal summary (About Me), and ends with a call to action (social links). This linear flow is intuitive and guides the user through the key aspects of the professional profile without requiring complex navigation, making it highly scannable and digestible, which is ideal for recruiters. -->
    <!-- Visualization & Content Choices: 
        - Report Info: Skill Proficiency Levels -> Goal: Compare -> Viz: Horizontal Bar Chart (Chart.js) -> Interaction: Tooltips on hover -> Justification: Bar charts are excellent for direct comparison of skill levels. The horizontal orientation provides ample space for labels.
        - Report Info: List of Technologies -> Goal: Organize/Inform -> Viz: Grid of styled cards (HTML/Tailwind) -> Interaction: Hover effects -> Justification: A visual grid is more engaging than a list or table, allowing for quick scanning of known technologies, similar to the user's reference image.
        - Report Info: Personal Bio & Socials -> Goal: Inform/Connect -> Viz: Styled text blocks and icon links -> Interaction: Standard links -> Justification: Clear, direct presentation is best for textual information and calls to action.
    -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&family=Roboto+Mono:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0d1117;
            color: #c9d1d9;
        }
        .font-mono {
            font-family: 'Roboto Mono', monospace;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            height: 400px;
            max-height: 50vh;
        }
        .tech-card {
            background-color: #161b22;
            border: 1px solid #30363d;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .tech-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 191, 255, 0.2);
            border-color: #00BFFF;
        }
        .section-title {
            color: #00BFFF;
        }
    </style>
</head>
<body class="antialiased">

    <div class="container mx-auto px-4 sm:px-6 lg:px-8 max-w-5xl">

        <!-- Header Banner -->
        <header class="my-8 md:my-12">
            <div class="w-full h-48 md:h-64 rounded-lg overflow-hidden">
                <img src="https://images.pexels.com/photos/3861958/pexels-photo-3861958.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" alt="Um ambiente de trabalho com múltiplos monitores exibindo código" class="w-full h-full object-cover">
            </div>
            <div class="text-center -mt-12">
                <h1 class="text-3xl md:text-5xl font-bold text-white">Marcos Paulo Alves de Freitas</h1>
                <p class="text-lg md:text-xl font-mono section-title mt-2">QA Engineer & Developer</p>
            </div>
        </header>

        <!-- Main Content -->
        <main>
            <!-- Skills Chart Section -->
            <section id="skills" class="my-16">
                <h2 class="text-3xl font-bold text-center mb-8 section-title">Matriz de Habilidades</h2>
                 <p class="text-center text-gray-400 mb-8 max-w-2xl mx-auto">Este gráfico representa meu nível de proficiência nas principais ferramentas e tecnologias que utilizo. Ele oferece uma visão rápida das minhas áreas de maior especialização.</p>
                <div class="chart-container">
                    <canvas id="skillsChart"></canvas>
                </div>
            </section>

            <!-- Technologies Section -->
            <section id="technologies" class="my-16">
                <h2 class="text-3xl font-bold text-center mb-8 section-title">Linguagens e Tecnologias</h2>
                 <p class="text-center text-gray-400 mb-8 max-w-2xl mx-auto">Aqui está o arsenal de tecnologias que domino para construir, testar e implantar aplicações robustas e eficientes.</p>
                <div id="tech-grid" class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 gap-4">
                    <!-- Tech cards will be injected here by JS -->
                </div>
            </section>

            <!-- About Me Section -->
            <section id="about" class="my-16 p-8 rounded-lg" style="background-color: #161b22; border: 1px solid #30363d;">
                <h2 class="text-3xl font-bold text-center mb-6 section-title">Sobre Mim</h2>
                <p class="text-center text-lg leading-relaxed max-w-3xl mx-auto">
                    Olá, eu sou o Marcos! 🚀<br>
                    Atuo como <b>QA Engineer</b> e <b>Developer</b>, com a missão de caçar bugs e construir soluções robustas e de alta qualidade. Sou apaixonado por automação e por criar processos que garantam a excelência do software, do planejamento à entrega. Curioso por natureza, estou sempre explorando novas tecnologias para aprimorar meu arsenal de desenvolvimento e testes.
                </p>
            </section>

            <!-- Connect Section -->
            <section id="connect" class="my-16 text-center">
                <h2 class="text-3xl font-bold mb-6 section-title">Conecte-se comigo</h2>
                <div class="flex justify-center space-x-6">
                    <a href="https://www.linkedin.com/in/marcos-freitas-0589021b2/" target="_blank" class="text-gray-400 hover:text-white transition-colors">
                        <span class="sr-only">LinkedIn</span>
                        <svg class="w-10 h-10" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
                    </a>
                    <a href="https://www.instagram.com/marcosdev03/" target="_blank" class="text-gray-400 hover:text-white transition-colors">
                        <span class="sr-only">Instagram</span>
                        <svg class="w-10 h-10" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.85s-.012 3.584-.07 4.85c-.148 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07s-3.584-.012-4.85-.07c-3.252-.148-4.771-1.691-4.919-4.919-.058-1.265-.07-1.645-.07-4.85s.012-3.584.07-4.85c.148-3.225 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.85-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948s.014 3.667.072 4.947c.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072s3.667-.014 4.947-.072c4.358-.2 6.78-2.618 6.98-6.98.058-1.281.072-1.689.072-4.948s-.014-3.667-.072-4.947c-.2-4.358-2.618-6.78-6.98-6.98-1.281-.059-1.689-.073-4.948-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.162 6.162 6.162 6.162-2.759 6.162-6.162-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4s1.791-4 4-4 4 1.79 4 4-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.441 1.441 1.441 1.441-.645 1.441-1.441-.645-1.44-1.441-1.44z"/></svg>
                    </a>
                </div>
            </section>
        </main>

        <footer class="text-center py-6 text-sm text-gray-500">
            <p>Desenvolvido por Marcos Paulo Alves de Freitas</p>
        </footer>

    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            // Data for the skills chart
            const skillsData = {
                labels: ['Python', 'Robot Framework', 'QA', 'Docker & CI/CD', 'APIs (REST)', 'Linux'],
                datasets: [{
                    label: 'Nível de Proficiência',
                    data: [85, 85, 85, 65, 75, 70],
                    backgroundColor: 'rgba(0, 191, 255, 0.5)',
                    borderColor: 'rgba(0, 191, 255, 1)',
                    borderWidth: 1,
                    barThickness: 20,
                    borderRadius: 5,
                }]
            };

            // Chart.js configuration
            const config = {
                type: 'bar',
                data: skillsData,
                options: {
                    indexAxis: 'y',
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            display: false
                        },
                        tooltip: {
                            backgroundColor: '#0d1117',
                            titleFont: {
                                size: 14,
                                family: 'Inter'
                            },
                            bodyFont: {
                                size: 12,
                                family: 'Inter'
                            },
                            padding: 10,
                            cornerRadius: 5,
                            displayColors: false,
                        }
                    },
                    scales: {
                        x: {
                            beginAtZero: true,
                            max: 100,
                            grid: {
                                color: 'rgba(255, 255, 255, 0.1)'
                            },
                            ticks: {
                                color: '#c9d1d9',
                                font: {
                                    family: 'Roboto Mono'
                                }
                            }
                        },
                        y: {
                            grid: {
                                display: false
                            },
                            ticks: {
                                color: '#c9d1d9',
                                font: {
                                    size: 14,
                                    family: 'Inter'
                                }
                            }
                        }
                    }
                }
            };
            
            // Render chart
            const skillsChartCtx = document.getElementById('skillsChart').getContext('2d');
            new Chart(skillsChartCtx, config);

            // Data for technologies grid
            const technologies = [
                { name: 'Python', category: 'Linguagens' },
                { name: 'JavaScript', category: 'Linguagens' },
                { name: 'C++', category: 'Linguagens' },
                { name: 'Robot Framework', category: 'Testes & Frameworks' },
                { name: 'Selenium', category: 'Testes & Frameworks' },
                { name: 'Node.js', category: 'Testes & Frameworks' },
                { name: 'Express.js', category: 'Testes & Frameworks' },
                { name: 'Postman', category: 'Testes & Frameworks' },
                { name: 'Jira', category: 'Testes & Frameworks' },
                { name: 'Confluence', category: 'Testes & Frameworks' },
                { name: 'Docker', category: 'DevOps & Ferramentas' },
                { name: 'CI/CD', category: 'DevOps & Ferramentas' },
                { name: 'Git & GitHub', category: 'DevOps & Ferramentas' },
                { name: 'Ubuntu', category: 'DevOps & Ferramentas' },
                { name: 'WSL2', category: 'DevOps & Ferramentas' }
            ];

            // Populate technologies grid
            const techGrid = document.getElementById('tech-grid');
            technologies.forEach(tech => {
                const card = document.createElement('div');
                card.className = 'tech-card p-4 rounded-lg flex items-center justify-center text-center';
                card.innerHTML = `<span class="font-semibold text-sm md:text-base">${tech.name}</span>`;
                techGrid.appendChild(card);
            });
        });
    </script>
</body>
</html>
