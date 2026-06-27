📑 Automação de Lista Mestre & Matriz de Treinamento
Este projeto foi desenvolvido em Python para automatizar a leitura de Procedimentos Operacionais Padrão (POPs) armazenados no Google Drive e alimentar a Lista Mestre de Documentos da Qualidade do laboratório, eliminando o erro humano e garantindo conformidade regulatória.

🚀 O que este robô faz?
[ Pasta no Drive ] ──► ( Robô lê POPs .docx / Docs ) ──► [ Extrai Item 3: Campo de Aplicação ] ──► 💾 Grava na Lista Mestre (Coluna G)
Varredura Inteligente: Conecta-se à pasta corporativa compartilhada e identifica todos os documentos de texto (sejam nativos do Google Docs ou arquivos do Microsoft Word .docx).

Leitura Automatizada: Abre os arquivos diretamente na memória do servidor e extrai todo o conteúdo textual (incluindo parágrafos e tabelas).

Extração via IA/Regex: Localiza especificamente o item "3. CAMPO DE APLICAÇÃO" de cada documento e isola o texto que descreve o público-alvo a ser treinado.

Cruzamento de Dados & Sincronização: Busca o título do documento dentro da planilha Lista Mestre e injeta a informação do treinamento diretamente na Coluna G (Quem deve ser treinado) da linha correspondente, preservando intactos os outros dados (versão, assinaturas, códigos).
