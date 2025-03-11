# Documentação com DAX Studio
Este script extrai o conteúdo do modelo do PBIX incluindo:

- Tabelas
- Colunas
- Ordenação das colunas
- Relacionamentos e cardinalidade
- Medidas e suas expressões
- Colunas calculadas
- Grupos de cálculos
- Formatos de medidas e colunas
- Queries M e DAX das tabelas
- Parâmetros do Modelo (Ex: Range Start/End) 

Instruções 
1. Com o projeto aberto no Power BI Desktop vá até a guia `Ferramentas Externas` e clique em [DAX Studio](https://daxstudio.org/) previamente instalado;
2. Copie o [script](extrai-modelo-dax-studio.dax) abaixo e cole na área da query no DAX Studio
3. Na barra de opções superior do DAX Studio, na divisão `Output` clique em `Results` e escolha a opção `Static`
4. Clique em `Run` na barra de navegação ou pressione `F5` no teclado
5. Escolha o local para salvar o arquivo gerado.

---

# AnalyzeInExcel

Analyze in Excel para Power BI Desktop, clique aqui e baixe uma versão mais recente:  [AnalyzeInExcel](https://www.sqlbi.com/tools/analyze-in-excel-for-power-bi-desktop/) 

O Analyze in Excel é uma ferramenta externa para o Power BI Desktop que conecta o Excel ao modelo de dados local do Power BI Desktop. O objetivo é permitir a criação de relatórios no Excel com apenas um clique. A primeira versão é básica, mas futuras atualizações podem adicionar funcionalidades sem comprometer a experiência simplificada.

**v1 - Abrir Excel**

Um botão nas Ferramentas Externas abre o Excel usando um arquivo ODC.
O usuário recebe uma Tabela Dinâmica vazia conectada ao modelo hospedado pelo Power BI Desktop.
Se o usuário criar um relatório mais complexo no Excel e salvar o arquivo, a conexão será perdida assim que o Power BI Desktop for fechado.
Ao reabrir o Power BI Desktop, a conexão será diferente, tornando inválida a conexão do arquivo salvo no Excel.

**v2 - Criar Relatório no Excel**

Um botão nas Ferramentas Externas cria um relatório no Excel usando Tabelas Dinâmicas e/ou Gráficos Dinâmicos.
O usuário recebe uma Tabela Dinâmica configurada, conectada ao modelo do Power BI Desktop.
O relatório pode ser baseado em um modelo, macro do Excel ou criado dinamicamente via Office SDK.
Se o usuário salvar o arquivo, a conexão será perdida ao fechar o Power BI Desktop.
Ao reabrir o Power BI Desktop, a conexão será diferente, invalidando a conexão do arquivo salvo no Excel.

**v3 - Abrir Relatório no Excel**

Um botão nas Ferramentas Externas abre um relatório existente no Excel ou cria um novo se for a primeira conexão com o relatório do Power BI.
Na primeira vez que o botão for usado em um arquivo PBIX, o usuário recebe uma Tabela Dinâmica configurada e conectada ao modelo do Power BI Desktop.
O relatório inicial pode ser baseado em um modelo, macro do Excel ou criado dinamicamente via Office SDK.
A conexão é perdida ao fechar o Power BI Desktop.
Ao reabrir o Power BI Desktop e usar a ferramenta, o arquivo do Excel é atualizado automaticamente para restaurar a conexão e, em seguida, aberto no Excel.

**v4 - Complemento do Excel para conectar ao Power BI Desktop**

Um suplemento do Excel, desenvolvido em VSTO, que abre o Power BI Desktop e conecta uma Tabela Dinâmica ao modelo de dados.
O usuário pode iniciar a conexão diretamente no Excel, abrindo um arquivo específico do Power BI Desktop se ainda não estiver aberto.
Se o arquivo do Excel foi salvo usando a ferramenta “Abrir Relatório no Excel”, o suplemento pode recuperar automaticamente o arquivo correto do Power BI Desktop para abrir.

---

# Bravo for Power BI

Bravo para Power BI é uma ferramenta gratuita de código aberto que ajuda você a criar um modelo do Power BI com uma interface de usuário simples. 

  - Analisar modelo: Encontre as colunas e tabelas mais caras
  - Formatar DAX: Formate suas medidas DAX
  - Gerenciar datas: Crie uma tabela de datas que você pode conectar a várias tabelas e aplique funções de inteligência de tempo às suas medidas.
  - Exportar dados: Exporte dados do Power BI para arquivos Excel e CSV.

Gratuito e de código aberto.

O Bravo não substitui ferramentas mais avançadas como DAX Studio e Tabular Editor.
O Bravo é para usuários que não precisam desse nível de complexidade.
Se você precisar de mais detalhes e opções, use outras ferramentas mais avançadas.
Mas quando a tarefa for simples, ou se você ainda estiver dando os primeiros passos com o Power BI, o Bravo está lá para ajudar.

clique aqui e baixe uma versão mais recente:  [Bravo](https://www.sqlbi.com/tools/bravo-for-power-bi/) 

---
# Tabular Editor

clique aqui e baixe:  [Tabular Editor](https://www.sqlbi.com/tools/tabular-editor/)

O **Tabular Editor** é uma alternativa ao SSDT para criar modelos tabulares no Analysis Services, mesmo sem um servidor de workspace.

O **Tabular Editor 2** é um projeto de código aberto que permite editar um arquivo BIM sem acessar os dados do modelo. 
Esse modo offline facilita ajustes rápidos no arquivo BIM, especialmente na manipulação de medidas, colunas calculadas, pastas de exibição, perspectivas e traduções.

O **Tabular Editor 3** é a versão comercial da ferramenta, oferecendo mais recursos de produtividade, um editor DAX avançado, uma interface aprimorada e suporte dedicado. 
O Tabular Editor não é produzido pela SQLBI, mas é altamente recomendado por ser o melhor ambiente de desenvolvimento para modelos semânticos e expressões DAX no Power BI e no Analysis Services.

O Tabular Editor é compatível com o nível 1200 ou superior (formato JSON), incluindo o nível 1500, necessário para grupos de cálculo.
Você pode baixar o executável e o código-fonte no projeto **Tabular Editor** no [GitHub](https://github.com/TabularEditor/TabularEditor/releases/tag/2.25).
