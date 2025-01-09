<section id="hunts">
    <h2>Hunts por Vocação e Nível</h2>
    <div class="tabs">
        <button class="tab-button" onclick="showTab('knight')">Cavaleiro</button>
        <button class="tab-button" onclick="showTab('sorcerer')">Feiticeiro</button>
        <button class="tab-button" onclick="showTab('druid')">Druida</button>
        <button class="tab-button" onclick="showTab('paladin')">Paladino</button>
    </div>

    <div id="knight" class="tab-content">
        <h3>Cavaleiro (Knight)</h3>
        <h4>Level 8-50</h4>
        <p><strong>Hunts:</strong> Rotworms (Venore ou Edron), Minotauros (Mintwallin ou Kazordoon), Crocodiles (Port Hope).</p>
        <p><strong>Runas:</strong> Nenhuma (melee-based).</p>
        <p><strong>Rotação:</strong> Use círculos no spawn, priorizando Exori em grupos.</p>

        <h4>Level 50-100</h4>
        <p><strong>Hunts:</strong> Larvas (Ankrahmun), Heroes (Edron), Orcs (Thais).</p>
        <p><strong>Runas:</strong> Utura para regeneração contínua.</p>
        <p><strong>Rotação:</strong> Faça luring e ataque em área (Exori).</p>

        <h4>Level 100+</h4>
        <p><strong>Hunts:</strong> Grim Reapers (Drefia), Dragon Lords (Darashia), Medusas (Port Hope).</p>
        <p><strong>Runas:</strong> Exura como cura emergencial.</p>
        <p><strong>Rotação:</strong> Lure poucos monstros por vez, priorizando ataques em área.</p>
    </div>

    <div id="sorcerer" class="tab-content hidden">
        <h3>Feiticeiro (Sorcerer)</h3>
        <!-- Conteúdo de Sorcerer -->
    </div>

    <div id="druid" class="tab-content hidden">
        <h3>Druida (Druid)</h3>
        <!-- Conteúdo de Druid -->
    </div>

    <div id="paladin" class="tab-content hidden">
        <h3>Paladino (Paladin)</h3>
        <!-- Conteúdo de Paladin -->
    </div>
</section>
/* Geral */
#hunts {
    margin: 20px auto;
    padding: 20px;
    background-color: #1f1f1f; /* Fundo escuro */
    color: #e0e0e0;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
}

#hunts h2 {
    text-align: center;
    color: #FFD700; /* Título dourado */
    border-bottom: 2px solid #FFD700;
    padding-bottom: 10px;
}

.tabs {
    display: flex;
    justify-content: center;
    margin-bottom: 20px;
}

.tab-button {
    background-color: #333;
    color: #FFD700;
    border: 1px solid #FFD700;
    padding: 10px 20px;
    margin: 0 5px;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
}

.tab-button:hover {
    background-color: #FFD700;
    color: #333;
}

.tab-content {
    display: none;
    margin-top: 20px;
}

.tab-content.active {
    display: block;
}

.hidden {
    display: none;
}

/* Estilo para Vocação */
.vocation h3 {
    color: #FFD700;
}

.vocation h4 {
    color: #ffcc00;
}

.vocation p {
    margin: 5px 0;
    line-height: 1.6;
}
<script>
    function showTab(tabId) {
        // Oculta todas as abas
        const tabs = document.querySelectorAll('.tab-content');
        tabs.forEach(tab => tab.classList.add('hidden'));

        // Remove a classe "hidden" da aba ativa
        document.getElementById(tabId).classList.remove('hidden');

        // Marcar o botão ativo (opcional)
        const buttons = document.querySelectorAll('.tab-button');
        buttons.forEach(btn => btn.classList.remove('active'));
        event.target.classList.add('active');
    }
</script>
