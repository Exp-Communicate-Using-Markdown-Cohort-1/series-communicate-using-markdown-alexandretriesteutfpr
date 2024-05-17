O que é o Markdown?
Concluído
100 XP
12 minutos
Markdown é uma linguagem de marcação que oferece uma abordagem enxuta para edição de conteúdo, protegendo os criadores de conteúdo da sobrecarga do HTML. Embora seja ótimo para renderizar o conteúdo exatamente como ele foi idealizado, o HTML ocupa muito espaço e pode ser difícil de trabalhar, mesmo em pequenas doses. A criação do Markdown trouxe um excelente meio-termo entre o poder do HTML para descrição de conteúdo e a facilidade de texto sem formatação para edição.

Nessa unidade, vamos conversar sobre a estrutura e a sintaxe do Markdown. Também abordaremos recursos do GFM (GitHub-Flavored Markdown), que são extensões de sintaxe que permitem integrar recursos do GitHub ao conteúdo.

 Observação

A finalidade desta unidade é dar uma ideia do que é o Markdown. Para uma análise mais detalhada, consulte os artigos "Descrição da sintaxe do Markdown" e "Especificação do Markdown com um sabor de GitHub" na seção Resumo no final desse módulo.

Enfatizar texto
A parte mais importante de qualquer comunicação no GitHub geralmente é o texto em si, mas como você mostra que algumas partes do texto são mais importantes do que outras?

Para usar itálico no texto, basta colocar o texto de destino entre asteriscos (*) ou sublinhados (_). Não deixe de fechar uma ênfase com o mesmo caractere usado para abri-la. Fique atento ao modo de combinar o uso de asteriscos e sublinhados. Veja os seguintes exemplos:

markdown

Copiar
This is *italic* text.
This is also _italic_ text.
Este é um texto em itálico. Esse também é um texto em itálico.

Crie texto em negrito usando dois asteriscos (**) ou dois sublinhados (__).

markdown

Copiar
This is **bold** text.
This is also __bold__ text.
Este é um texto em negrito. Este também é um texto em negrito.

Você também pode misturar tipos de ênfase diferentes.

markdown

Copiar
_This is **italic and bold** text_ using a single underscore for italic and double asterisks for bold.
__This is bold and *italic* text__ using double underscores for bold and single asterisks for italic. 
Este é um texto em itálico e negrito usando um só sublinhado para itálico e dois asteriscos para negrito. Este é um texto em negrito e itálico usando dois sublinhados para negrito e um asterisco para itálico.

Para usar um asterisco literal, preceda-o com um caractere de escape, que no GFM é uma barra invertida (\). Este exemplo resulta em sublinhados e asteriscos sendo mostrados na saída.

markdown

Copiar
\_This is all \*\*plain\*\* text\_.
_Tudo isto é um texto *sem formatação**_.

Declarar títulos
O HTML fornece títulos de conteúdo, como a tag <h1>. Em Markdown, isso tem suporte por meio do símbolo #. Basta usar um # para cada nível de título de 1 a 6.

markdown

Copiar
###### This is H6 text
Este é o texto H6
Criar links para imagens e sites
Os links para imagens e sites usam uma sintaxe semelhante.

markdown

Copiar
![Link an image.](/learn/azure-devops/shared/media/mara.png)
Link an image.

markdown

Copiar
[Link to Microsoft Training](/training)
Link para o Microsoft Training

Criar listas
Você pode definir listas ordenadas ou não ordenadas. Você também pode definir itens aninhados por meio de recuos.

As listas ordenadas começam com números.
As listas não ordenadas podem usar asteriscos ou traços (-).
Aqui está o Markdown de uma lista ordenada:

markdown

Copiar
1. First
1. Second
1. Third
Resultado:

Primeiro
Segundo
Terceiro
markdown

Copiar
- First
  - Nested
- Second
- Third
Aqui está o Markdown de uma lista não ordenada:

Primeiro
Aninhado
Segundo
Terceiro
Criar tabelas
Você pode construir tabelas usando uma combinação de barras verticais (|) para quebras de coluna e traços (-) para designar a linha anterior como um cabeçalho.

markdown

Copiar
First|Second
-|-
1|2
3|4
Primeiro	Segundo
1	2
3	4
Texto da citação
Você pode criar blockquotes usando o caractere maior que (>).

markdown

Copiar
> This is quoted text.
Este é um texto de referência.

Preencher as lacunas com HTML incorporado
Se você se deparar com uma situação de HTML que não é compatível com o Markdown, você pode usar o HTML incorporado.

markdown

Copiar
Here is a<br />line break
Esta é uma
quebra de linha

Trabalhe com código
O Markdown fornece um comportamento padrão para trabalhar com blocos de código embutidos delimitados pelo caractere de crase (`). Ao ser decorado com esse caractere, o texto é renderizado como código.

markdown

Copiar
This is `code`.
Este é um code.

Se tiver um segmento de código que abrange várias linhas, você poderá usar três crases (```) antes e depois para criar um bloco de código isolado.


Copiar
```markdown
var first = 1;
var second = 2;
var sum = first + second;
```

Copiar
var first = 1;
var second = 2;
var sum = first + second;
O GFM estende esse suporte com realce de sintaxe para linguagens populares. Basta especificar a linguagem como parte da primeira sequência de crases.


Copiar
```javascript
var first = 1;
var second = 2;
var sum = first + second;
```
JavaScript

Copiar
var first = 1;
var second = 2;
var sum = first + second;
Problemas de referência cruzada e solicitações de pull
O GFM é compatível com o uso de uma variedade de formatos de código curto para facilitar a criação de links para problemas e solicitações de pull. A maneira mais fácil de fazer isso é usar o formato #ID, como #3602. O GitHub ajustará automaticamente os links mais longos para esse formato se você quiser colá-los. Você também poderá seguir convenções adicionais, por exemplo, se estiver trabalhando com outras ferramentas ou se quiser especificar outros projetos/branches.

Tipo de referência	Referência bruta	Link curto
URL do problema ou da solicitação de pull	https://github.com/desktop/desktop/pull/3602	#3602
# e o número do problema ou da solicitação de pull	#3602	#3602
GH- e o número do problema ou da solicitação de pull	GH-3602	GH-3602
Username/Repository# e o número do problema ou da solicitação de pull	desktop/desktop#3602	desktop/desktop#3602
Para obter mais informações, consulte o artigo "Referências e URLs com links automáticos" na unidade Resumo no final desse módulo.

Links para commits específicos
Você pode criar um link para um commit colando a respectiva ID ou, simplesmente, usando o respectivo algoritmo de hash seguro (SHA).

Tipo de referência	Referência bruta	Link curto
URL da confirmação	https://github.com/desktop/desktop/commit/	
8304e9c271a5e5ab4fda797304cd7bcca7158c87	8304e9c	
SHA	8304e9c271a5e5ab4fda797304cd7bcca7158c87	8304e9c
User@SHA	desktop@8304e9c271a5e5ab4fda797304cd7bcca7158c87	desktop@8304e9c
Username/Repository@SHA	desktop/desktop@8304e9c271a5e5ab4fda797304cd7bcca7158c87	desktop/desktop@8304e9c
Mencionar usuários e equipes
Digitar um símbolo @ seguido de um nome de usuário do GitHub enviará a essa pessoa uma notificação relativa ao comentário. Isso é chamado de uma "@menção", porque você está mencionando o indivíduo. Você também pode usar @mention com equipes dentro de uma organização.

markdown

Copiar
@githubteacher
@githubteacher

Monitorar listas de tarefas
Você pode criar listas de tarefas dentro de problemas ou solicitações de pull usando a sintaxe abaixo. Isso pode ser útil para acompanhar o progresso quando usado no corpo de um problema ou solicitação de pull.

markdown

Copiar
- [x] First task
- [x] Second task
- [ ] Third task
A GitHub task list.
