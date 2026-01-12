Canva Focus - Plugin QGIS
==========================

Sobre
-----
O Canva Focus é um plugin para QGIS que ajuda a visualizar e controlar o foco na área central do mapa. Permite definir uma zona de borda ajustável, visualizar o centro do mapa e centralizar automaticamente ao clicar fora da zona de foco.

Autor: Alberto Rodrigues
Email: betorodrigues@msn.com
Versão: 1.0
Licença: GNU General Public License v2 ou superior

Repositório: https://github.com/skavazza/Canva-Focus
Issues: https://github.com/skavazza/Canva-Focus/issues


Funcionalidades
---------------
• Visualizar uma borda ajustável que delimita a zona de foco central do mapa
• Ajustar o tamanho da zona de foco através de um slider (valores de 100 a 150)
• Ativar/desativar o modo de foco com um botão toggle
• Visualizar o centro exato da zona de foco com um marcador em cruz
• Centralizar automaticamente o mapa ao clicar fora da zona de foco quando o modo estiver ativado

Ideal para trabalhos que requerem precisão no posicionamento e visualização do centro do mapa.


Requisitos
----------
• QGIS versão 3.0 ou superior


Instalação
----------
1. Faça o download ou clone do repositório:
   git clone https://github.com/skavazza/Canva-Focus.git

2. Copie a pasta do plugin para o diretório de plugins do QGIS:
   Windows: C:\Users\<username>\AppData\Roaming\QGIS\QGIS3\profiles\default\python\plugins\
   Linux: ~/.local/share/QGIS/QGIS3/profiles/default/python/plugins/
   macOS: ~/Library/Application Support/QGIS/QGIS3/profiles/default/python/plugins/

3. Renomeie a pasta para "canva_focus" (se necessário)

4. Compile os recursos (se necessário):
   pyrcc5 resources.qrc -o resources.py

5. Reinicie o QGIS ou recarregue os plugins

6. Ative o plugin em: Complementos > Gerenciar e Instalar Complementos > Instalados


Como Usar
---------
1. Após ativar o plugin, acesse: Complementos > Canva Focus > Foco no canva
   Ou use o ícone na barra de ferramentas

2. O dockwidget "Canva Focus" será exibido com dois controles:
   • Slider: Ajusta o tamanho da zona de foco (100 = menor, 150 = maior)
   • Botão Toggle: Ativa (O - verde) ou desativa (C - vermelho) o modo de foco

3. Quando ativado:
   • Uma borda pontilhada será exibida no mapa delimitando a zona de foco
   • Um marcador em cruz mostrará o centro exato da zona
   • Ao clicar fora da zona de foco, o mapa centralizará automaticamente nesse ponto

4. Use o slider para ajustar o tamanho da zona conforme necessário


Desenvolvimento
---------------
Para desenvolvedores que desejam contribuir ou modificar o plugin:

Estrutura do Projeto:
• canva_focus.py - Arquivo principal do plugin
• canva_focus_dockwidget.py - Implementação do dockwidget e classes de controle
• canva_focus_dockwidget_base.ui - Interface gráfica (Qt Designer)
• resources.qrc - Recursos do plugin
• metadata.txt - Metadados do plugin

Compilar recursos:
pyrcc5 resources.qrc -o resources.py

Executar testes:
make test

Mais informações sobre desenvolvimento PyQGIS:
http://www.qgis.org/pyqgis-cookbook/index.html


Changelog
---------
Versão 1.0 - 2026-01-11
• Implementação inicial do plugin
• Controle de borda ajustável com slider
• Botão toggle para ativar/desativar o modo de foco
• Visualização do centro da zona de foco com marcador
• Interceptação de cliques para centralização automática do mapa
• Interface dockwidget com controles intuitivos


Suporte
-------
Para reportar bugs, solicitar funcionalidades ou obter ajuda:
• Issues: https://github.com/skavazza/Canva-Focus/issues
• Email: betorodrigues@msn.com


Licença
-------
Este programa é software livre; você pode redistribuí-lo e/ou modificá-lo
sob os termos da GNU General Public License conforme publicada pela
Free Software Foundation; seja a versão 2 da Licença, ou (a seu critério)
qualquer versão posterior.

Copyright (C) 2026 Alberto Rodrigues
