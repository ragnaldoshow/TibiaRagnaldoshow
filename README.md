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
