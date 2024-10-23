# Sistema-de-Market-LUA

![Lua](https://img.shields.io/badge/Lua-2C2D72?style=for-the-badge&logo=lua&logoColor=white)&nbsp;
![Tibia](https://img.shields.io/badge/Tibia-DC322F?style=for-the-badge)&nbsp;
![Otc](https://img.shields.io/badge/Otcv8Cliente-404D59?style=for-the-badge)&nbsp;
![Script](https://img.shields.io/badge/Script-DB7093?style=for-the-badge)&nbsp;
![WebSockect](https://img.shields.io/badge/WebSocket-0081CB?style=for-the-badge&logo=material-ui&logoColor=white)&nbsp;
#

Este script em Lua foi desenvolvido para o OTCv8, uma framework alternativo e open-source para o jogo Tibia. Ele é exclusivamente compatível com servidor alternativo de Tibia.
#

# 1. Funcionalidades do Script
  * Registro automático de novos itens.
  * Alertas via WebSocket para usuários no Discord.
  * Filtragem de itens por preço ou upgrades (duas moedas: gold e premium points).
</br>
<div>
  <span>Verde: Verde: Liga/desliga a macro para o script funcionar.</span><br>
  <span>Vermelho: Abre a janela de configuração personalizada (OTUI) para alertas e IDs de Discord.</span><br>
  <span>Azul: Configura o intervalo de verificação do market.</span><br>
  <span>Roza: Define o "cooldown" do loop (em minutos). </span>
</div>
<div align="center">
  <img src="https://imgur.com/pYDV0dY.png" alt="Texto Alternativo">
</div>

**CONDIÇÕES OBRIGATÓRIAS:**
* O script precisa estar ativo.
* Para os alertas funcionarem, os nomes e IDs dos players no Discord devem ser configurados.

# 2. Janela de Configuração dos Alertas

* Discord Members
   - Informações necessárias:
     - 1: Nome
     - 2: ID do discord

* Items
  - Os itens são registrados automaticamente pelo script com nome e ID.

* Alerts
  É necessário selecionar um item para ativar o alerta.
     - Dados obrigatórios para ser adicionado:
     - Nome do membro
     - Tipo de moeda para o alerta

Na janela de configurações, existem campo de textos que podem ser digitadas os valores necessário para adicionar no sistema.
<div align="center">
  <img src="https://imgur.com/CAfwAG1.png" alt="Texto Alternativo">
</div>

# 3. Funcionamento do Script
Com o script ativo, o personagem se move até o market e verifica os itens à venda. Ao selecionar um player, o script lê o nome, ID, valores e quantidades dos itens.
<div align="center">
  <img src="https://imgur.com/JnI38wh.png" alt="Player Market Window">
</div>
O script então envia um HTTP via WebSocket para o Discord com os detalhes da venda.</br>
Status Verde: Foi alertado um player.</br>
Status Vermelho: Nenhum player é para ser alertado.
<div align="center">
  <img src="https://imgur.com/uBPKbuL.png" alt="Player Market Window">
</div>

