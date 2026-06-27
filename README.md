📑 Automação de Lista Mestre & Matriz de Treinamento
Este projeto foi desenvolvido em Python para automatizar a leitura de Procedimentos Operacionais Padrão (POPs) armazenados no Google Drive e alimentar a Lista Mestre de Documentos da Qualidade do laboratório, eliminando o erro humano e garantindo conformidade regulatória.

🚀 O que este robô faz?
[ Pasta no Google Drive ] ──► ( Robô lê POPs .docx / Docs ) ──► [ Extrai Item 3: Campo de Aplicação ] ──► 💾 Grava na Lista Mestre (Coluna G)
Varredura Inteligente: Conecta-se à pasta corporativa compartilhada e identifica todos os documentos de texto (sejam nativos do Google Docs ou arquivos do Microsoft Word .docx).

Leitura Automatizada: Abre os arquivos diretamente na memória do servidor e extrai todo o conteúdo textual (incluindo parágrafos e tabelas).

Extração via IA/Regex: Localiza especificamente o item "3. CAMPO DE APLICAÇÃO" de cada documento e isola o texto que descreve o público-alvo a ser treinado.

Cruzamento de Dados & Sincronização: Busca o título do documento dentro da planilha Lista Mestre e injeta a informação do treinamento diretamente na Coluna G (Quem deve ser treinado) da linha correspondente, preservando intactos os outros dados (versão, assinaturas, códigos).

🛠️ Tecnologias Utilizadas
Python 3: Linguagem base do script.

Google Drive & Sheets APIs v3/v4: Para comunicação direta e segura com o ecossistema Google.

PyPDF & Python-Docx: Bibliotecas especialistas na extração de textos de arquivos PDF e Word sem desformatar a estrutura.

📖 Como Executar (Manual do Usuário)
O script foi desenhado para ser executado em ambiente de nuvem de forma simples, necessitando apenas de três passos por parte do usuário:

Acessar o Ambiente: Abra este caderno do Google Colab.

Disparar a Execução: No menu superior, clique em Ambiente de execução (Runtime) e selecione a opção Executar tudo (Run all).

Autorizar Credenciais: Uma janela pop-up do Google será exibida. Clique em "Permitir" utilizando a conta institucional que possui acesso à pasta da Qualidade.

⚠️ Nota de Segurança: O script roda de forma 100% segura dentro dos servidores do Google. Ele herda rigorosamente as permissões do usuário que o executa, garantindo que nenhum dado sensível saia do ambiente controlado do laboratório.

⚙️ Configurações do Desenvolvedor
Caso seja necessário alterar a pasta ou a planilha de destino, as variáveis de configuração estão no topo do código:

PASTA_ID: O identificador exclusivo da pasta onde os POPs são depositados.

LISTA_MESTRE_ID: O ID extraído da URL da Planilha Oficial de Controle.

Mapeamento de Colunas: O código está calibrado para ler códigos/títulos nas colunas A/B e salvar o resultado na coluna G da aba 'Lista Mestre'.

🛡️ Próximos Passos do Projeto
Implementar o bloqueio total de edição direta na Lista Mestre para os usuários.

Adicionar a função de criação de novas linhas automáticas ao detectar novos arquivos na pasta.

Criar uma interface visual de botão único ("Sincronizar") para o usuário final.
