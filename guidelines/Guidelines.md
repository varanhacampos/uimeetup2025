# Fundamentals

## Colors
### Description
Colors define brand identity, semantic meaning, and structural hierarchy. Mística uses brand palettes, semantic palettes and neutrals, with built-in support for light and dark color schemes and contextual variants.

For this context, always use the brand "Vivo-new" and it's tokens, by using the CSS document or figma variables brand "Vivo-new".

### Rules of Use
- Use brand colors for primary actions and highlights.
- Use semantic colors (success, warning, error) for status messaging.
- Use neutral palette for backgrounds and text hierarchy.
- Respect contrast ratios defined in WCAG 2.2.
- Use inverse contexts when placing components over colored or media backgrounds.

### Decision Examples
- If a button appears over brand background → use inverse variant.
- If a section needs emphasis → use backgroundAlternative.
- If placing text over an image → use textPrimaryInverse or textSecondaryInverse.

## Typography
### Description
Typography is structured using text-presets, which define font size, weight, and line height per device type (mobile/desktop).

### Rules of Use
- Always use text-presets; do not manually override sizes.
- Maintain hierarchy visually through preset selection.
- Large sizes (preset 5+) have weight controlled by brand skin.

### Decision Examples
- Use text-preset-6 for section titles.
- Use text-preset-3 for body text.
- Use preset-10 only for major headlines or hero areas.

## Spacing
### Description
Spacing follows a vertical rhythm with defined levels (L1–L4). Tokens ensure consistency across flows.

### Rules of Use
- Use spacing tokens instead of fixed pixels.
- Apply Level 1 spacing around header/footer blocks.
- Apply Level 2 spacing between major content blocks.
- Apply Level 3 spacing between title and content inside a block.
- Apply Level 4 spacing between components inside a block.

### Decision Examples
- When grouping related cards → use Level 3 (16px/24px).
- When separating sections → use Level 2 (40px mobile, 48px desktop).

## Layouts
### Description
Layouts define responsive grids, breakpoints, and flow structures.

### Rules of Use
- Use responsive layout to center content across breakpoints.
- Use grid templates (6+6, 8+4, 3+9) depending on content type.
- Use horizontal scroll only when content overflow is expected.
- Align items with Align component when needed.

### Decision Examples
- For image + text → use grid 6+6.
- For main content + aside → use grid 8+4.
- For left navigation → use grid 3+9.

## Motion
### Description
Motion provides meaning through easing and duration tokens. Animations should be subtle and accessible.

### Rules of Use
- Use FadeIn for newly added content.
- Use standard easing curves for UI transitions.
- Disable autoplay for videos when prefers-reduced-motion is enabled.
- Show video playback controls if duration > 5s or autoplay disabled.

### Decision Examples
- Use 1000ms fade for onboarding transitions.
- Use shorter transitions (150–250ms) for micro-interactions.

## Iconography
### Description
Icons come in Light, Regular, and Filled styles, automatically adapting to brand skins.

### Rules of Use
- Use Regular for default sizes (24px).
- Use Light for large icons (>48px).
- Use Filled only for low-resolution environments (e.g., TV).
- Icons must be consistent within a section.

### Decision Examples
- Use Light style in hero illustrations.
- Use Regular style for navigation and actions.

---

# Layout & Grid Guidelines

Este guia define o comportamento do layout responsivo, breakpoints, grid e templates estruturais utilizados no projeto. Ele garante consistência visual, escalabilidade e previsibilidade em todas as interfaces.

## Breakpoints

### sm:
- Intervalo: 320 a 767 px
- Margem horizontal: 16 px

### md:
- Tablets
- Intervalo: 768 a 1023 px
- Margem horizontal: 32 px

### lg:
- Desktops pequenos
- Intervalo: 1024 a 1511 px
- Margem horizontal: 48 px

### xl:
- Desktops maiores
- Intervalo: 1512 px ou mais
- Margem horizontal: Automática (conteúdo centralizado)

## Regras gerais de breakpoints:

- As margens laterais aumentam conforme a largura do dispositivo.
- Em large desktop, a margem é fluida para centralizar o conteúdo.
- As margens definem o limite horizontal máximo do grid.

## Grid System

### sm:
- Número de colunas: 1
- Tamanho das colunas: Fluido
- Gutter: Nenhum

### md:
- Número de colunas: 1
- Tamanho das colunas: Fluido
- Gutter: Nenhum

### lg:
- Número de colunas: 12
- Tamanho das colunas: Fluido
- Gutter: 24 px

### xl:
- Número de colunas: 12
- Tamanho das colunas: 96 px por coluna
- Gutter: 24 px

## Regras gerais do grid:

Em mobile e tablet, o grid é sempre uma coluna única.

Em desktop, o layout passa a utilizar 12 colunas responsivas.

Em large desktop, cada coluna tem largura fixa de 96 px.

Os gutters permanecem sempre em 24 px em telas amplas.

## Grid Layout Templates

Os templates abaixo representam combinações pré-definidas de colunas para organizar o conteúdo de forma consistente.

### Template 6 + 6
- Distribuição equilibrada meio a meio.

Ideal para:
- Imagem + texto
- Heros simples
- Seções com equilíbrio visual

### Template 8 + 4
- Coluna principal ampla e coluna auxiliar estreita.

Ideal para:
- Conteúdo + aside
- Navegação secundária
- Blocos complementares

### Template 4 + 6
- Coluna menor seguida de coluna principal.

Ideal para:
- Master-detail
- Listagens + conteúdo expandido

### Template 5 + 4
- Template exclusivo para full screen funnel.

Ideal para:
- Step-by-step
- Fluxos guiados
- Processos de conversão

### Template 3 + 9
- Coluna estreita com coluna principal expandida.

Ideal para:
- Navegação lateral
- Filtros
- Ferramentas com menu persistente

## Comportamento Responsivo

### Mobile e Tablet

Todo template se transforma automaticamente em uma única coluna vertical.

A ordem de leitura deve respeitar a hierarquia do conteúdo.

Proporções horizontais deixam de ser consideradas.

### Desktop e Large Desktop

Os templates assumem sua proporção de colunas original.

Deve-se respeitar:

Margens definidas por breakpoint

Gutter fixo de 24 px

Limite total de 12 colunas

## Boas Práticas
- Utilize sempre o grid oficial para composições.
- Evite expandir conteúdo para a largura total em large desktop.
- Priorize legibilidade em telas pequenas.
- Respeite as proporções originais dos templates para garantir consistência.

Evite combinações de colunas fora dos templates definidos.

--------------

# Components

--------------

# Patterns

--------------

# Vivaz e Tom de Voz

## Sobre o Vivaz
O **Vivaz** é o Content Design System da Vivo. Nele, você encontra tudo o que precisa para escrever de acordo com o jeito Vivo nos produtos digitais – desde diretrizes de tom de voz até padrões de comunicação.

As diretrizes do Vivaz apoiam as equipes no dia a dia e garantem uma comunicação consistente e alinhada em todos os pontos de contato.

## Sobre o nome Vivaz
O nome **Vivaz** simboliza algo duradouro, cheio de energia e em constante evolução. Assim como a língua portuguesa, nosso Design System está sempre vivo e se adapta às necessidades dos nossos usuários.

---

# Content Design

## Diretrizes gerais de Tom de Voz na Vivo

### Premissas de UX Writing
As premissas de UX Writing ajudam a tomar decisões de conteúdo que refletem nossos valores e atendem às necessidades das pessoas usuárias.

- **Clareza:** Linguagem simples, sem jargões ou termos técnicos desnecessários, garantindo que todos compreendam.
- **Concisão:** Mensagens diretas e eficientes, evitando rodeios e mantendo o foco na necessidade do usuário.
- **Utilidade:** Informações relevantes que orientam os próximos passos.
- **Consistência:** Padrões de voz, tom e estilo uniformes em toda a comunicação.
- **Acessibilidade:** Conteúdos inclusivos que seguem boas práticas de acessibilidade.

### Premissas de conteúdo na Vivo
Nossas diretrizes garantem uma comunicação simples, direta e alinhada à personalidade da Vivo.

Somos uma marca de tecnologia que transforma a conexão das pessoas com o mundo, oferecendo experiências mais humanas e alinhadas às suas necessidades. Por isso, nosso tom de voz é **Human Tech**, conectando tecnologia e pessoas de forma autêntica e relevante.

Nosso jeito de comunicar reflete:

- **Agilidade e simplicidade:** Falamos de forma objetiva, com palavras fáceis e sem complicar.
- **Benefício da tecnologia:** Traduzimos a tecnologia em vantagens reais para as pessoas.
- **Inovação e digital:** Usamos linguagem da internet e do mundo tech, mantendo frases curtas e informais.
- **Tecnologia afetiva:** Democratizamos o acesso à tecnologia, priorizando as relações humanas.

### Tom de Voz Vivo
Nosso tom de voz reflete quem somos e como nos comunicamos. Ele se baseia em cinco atributos principais:

- **Atuais:** Estamos sempre antenados às tendências e promovemos transformação tecnológica.
- **Otimistas:** Expressamos confiança, leveza e inspiramos realização.
- **Inclusivos:** Colocamos as pessoas no centro, acolhendo e oferecendo soluções.
- **Empáticos:** Ajudamos e incentivamos, criando um diálogo próximo e compreensível.
- **Acessíveis:** Simplificamos temas complexos e explicamos termos técnicos quando necessário.

---

## Diretrizes Gerais de Linguagem da Vivo

### Linguagem Conversacional
Use textos conversacionais, descomplicados e acessíveis, próximos da forma como as pessoas falam no dia a dia.

**Exemplos Corretos:**
- "Quer saber mais? A gente explica!"
- "Escolha a assinatura que combina com você."

**Exemplos Incorretos:**
- "Para obter mais informações, consulte o guia."
- "Selecione a assinatura de acordo com suas necessidades."

---

## Linguagem Informativa
Seja claro e direto, fornecendo as informações necessárias de forma objetiva.

**Exemplos Corretos:**
- "A instalação do Vivo Fibra leva até 5 dias úteis."
- "Para suporte, entre em contato pelo app Meu Vivo."

**Exemplos Incorretos:**
- "O processo de instalação pode variar conforme disponibilidade."
- "Caso precise de ajuda, consulte nossos canais de atendimento."

---

## Linguagem Transparente
Seja honesto e evite ambiguidades, transmitindo confiança.

**Exemplos Corretos:**
- "A cobrança será feita todo mês em sua fatura."
- "Seu plano inclui 10GB de internet e ligações ilimitadas."

**Exemplos Incorretos:**
- "A cobrança será feita periodicamente."
- "Você terá internet e ligações ilimitadas."

---

## Linguagem Simples
Utilize palavras fáceis e frases curtas para garantir uma comunicação acessível.

**Exemplos Corretos:**
- "Ative sua linha em poucos passos."
- "Baixe a fatura no app."

**Exemplos Incorretos:**
- "Realize a ativação do seu plano em nosso portal."
- "Para efetuar o download da sua fatura, acesse a plataforma."

---

## Tempos Verbais
Usamos tempos verbais simples, sempre no presente e  expressos por uma só palavra.

**Exemplos Corretos:**
- "Nós atendemos as suas solicitações."
- "Você vai receber uma ligação da equipe técnica."

**Exemplos Incorretos:**
- "Nós temos atendido as suas solicitações."
- "Você receberá uma ligação da equipe técnica."

**Exceção:**
- Evitamos tempos verbais no futuro. Preferimos a construção "ir + verbo no infinitivo" para tornar a comunicação mais natural.
**Exemplo correto*
- Você vai receber um SMS
**Exemplo incorreto**
- Você receberá um SMS

---

## Voz Ativa
Usamos a voz ativa para reforçar que as pessoas estão no centro da comunicação.

**Exemplos Corretos:**
- "Você ativou o seu Vivo Chip."
- "A equipe técnica resolveu o problema."

**Exemplos Incorretos:**
- "O Vivo Chip foi ativado por você."
- "O problema foi resolvido pela equipe técnica."

---

## Modos Verbais
Damos preferência ao uso de verbos no infinitivo, pois indicam a ação a ser executada.

**Exemplos Corretos:**
- "Fazer nova assinatura."
- "Baixar fatura."

**Exemplos Incorretos:**
- "Assine novo plano."
- "Baixe sua fatura."

**Exceções:**
- Botões e entrypoints devem sempre usar o verbo no infinitivo.
- O uso do modo imperativo deve ser equilibrado e aplicado apenas em instruções diretas.

---

## Pronomes
Falamos em nome da Vivo usando o gênero feminino e a primeira pessoa do plural.

**Exemplos Corretos:**
- "Nós estamos aqui para ajudar você."

**Exemplos Incorretos:**
- "A Vivo está aqui para ajudar você."

**Exceção:**
- A terceira pessoa do singular pode ser usada em materiais institucionais e publicitários.

---

## Pronomes dos Clientes
Evite marcações de gênero, preferindo o uso de "você" ou o nome da pessoa.

**Exemplos Corretos:**
- "Você já pode baixar sua fatura."
- "Olá, José. Sua fatura chegou."

**Exemplos Incorretos:**
- "O senhor já pode baixar sua fatura."
- "Prezado José."

---

## Meu ou Seu/Sua
A escolha entre "meu/minha" e "seu/sua" depende do contexto da interação.

- **Meu/minha:** Quando a pessoa usuária está gerenciando algo que é dela, como em "Meu plano Vivo" ou "Minha fatura".
- **Seu/Sua:** Quando a Vivo se dirige à pessoa usuária, como em "Sua fatura está disponível" ou "Seu plano foi atualizado".

**Exemplos Corretos:**
- "Acesse sua fatura pelo app."
- "Confira em Meu histórico de consumo."

**Exemplos Incorretos:**
- "Acesse minha fatura pelo app."
- "Veja seu histórico de consumo."

---

## Pra e Para
O uso de "pra" é permitido em comunicações mais informais e próximas, enquanto "para" deve ser usado em contextos mais formais.

**Use "pra" nos fluxos felizes, como:**
- Ao oferecer um novo produto ou serviço.
- Ao comunicar uma oferta, vantagem ou benefício.
- Em jornadas de contratação de planos.

**Exemplos:**
- "Temos uma oferta especial pra você!"
- "Estamos aqui pra ajudar."

**Use "para" em situações formais, como:**
- Cancelamentos.
- Negociação de fatura.
- Mensagens de erro ou suporte técnico.

**Exemplos:**
- "Estamos processando sua solicitação para cancelamento."
- "Para suporte técnico, acesse nosso portal."

---


## Formal e Informal
A comunicação deve ser próxima e acessível, mas sem exagerar na informalidade.

**Exemplos Corretos:**
- "Nossos consultores estão prontos para ajudar você."

**Exemplos Incorretos:**
- "Tá na mão! Conte com a Vivo pra tudo."

**Exceções:**
- Mensagens de cunho legal ou técnico, como preços, parcelas, confirmações de compra, atendimento, perda, roubo e outras situações difíceis exigem um tom mais neutro e formal.

---
## Diretrizes para Uso de Verbos no Infinitivo
Na Vivo, **sempre utilizamos verbos no infinitivo** (terminados em -ar, -er, -ir) em textos de interfaces, comunicações e conteúdos digitais.  
**Objetivo**: Garantir clareza, neutralidade e alinhamento com o tom de voz **Human Tech**.

**Exemplos Corretos:**
- "Ativar pacote" (em vez de "Ative seu pacote")
- "Conhecer benefícios" (em vez de "Conheça os benefícios")
- "Falar com atendente" (em vez de "Fale com nosso atendente")

**Exemplos Incorretos:**
- "Ative já seu pacote" (imperativo)
- "Você receberá um e-mail" (futuro)
- "Clique aqui para ativar" (imperativo implícito)

**Exceções Permitidas**
1. Instruções Muito Específicas
O **imperativo** pode ser usado apenas em cenários críticos que exigem ação imediata e inequívoca.
**Exemplo**:  
- "Desligue o aparelho antes de instalar o chip." (segurança física)
- "Pressione o botão de emergência." (cenário de risco)

2. Nomes de Seções ou Serviços
Quando o texto **não é uma ação direta**, mas identifica uma seção:
**Exemplo**:  
- "Suporte Técnico" (não "Suporte Técnico Acesse")
- "Vivo Travel" (nome próprio)

3.  Botões e Call-to-Actions:     
- Sempre use infinitivo: "Contratar pacote", "Falar com atendente".

4. Telas de Instrução:     
- Prefira infinitivo: "Inserir chip no slot indicado."
- Reserve imperativo apenas para emergências.

5. **Mensagens Automáticas**:  
- Exemplo: "Para consultar saldo, digitar *555."

**Justificativa:** 
- O infinitivo é mais neutro e compreensível para todos os públicos, incluindo pessoas neurodivergentes.
- **Consistência**: Alinhamento com as premissas de **clareza** e **simplicidade** do Vivaz.
- **Experiência do Usuário**: Evita tom impositivo, mantendo a abordagem **empática** da marca.

---

## Clareza
Uma ideia por bloco de texto, evitando sobrecarga de informação.

**Exemplos Corretos:**
- "Escolha a assinatura ideal para você."

**Exemplos Incorretos:**
- "Escolha a assinatura e aproveite as vantagens agora."

---

## Inclusão
Escreva textos acessíveis para diferentes níveis de conhecimento, oferecendo contexto.

**Exemplos Corretos:**
- "Escolha a assinatura que mais combina com o seu perfil."

**Exemplos Incorretos:**
- "Selecione uma das opções apresentadas."

---

## Evite Orações Negativas
Prefira construir frases afirmativas para facilitar o entendimento.

**Exemplos Corretos:**
- "Confira os detalhes antes de finalizar a compra."

**Exemplos Incorretos:**
- "Não se esqueça de verificar os detalhes antes de finalizar a compra."

---

## A gente não usa qualquer texto que lembre empresas concorrentes, como a saudação "Oi", a frase “É claro que..." e também "a sua net...".

---

## Emojis
Temos uma seção específica sobre emojis em estilos e formatação.

---

# Diretrizes de Produtos e Serviços Vivo

## **Produtos Vivo**

### **App Vivo**

#### **Como a gente fala**
No final de 2022, a Vivo fez uma mudança no branding, adotando o **Vivinho** como prioritário nas comunicações. Apesar disso, o nome do nosso app segue o jeito mais habitual de ser falado pelas pessoas: **App Vivo**.

**Exemplos Corretos:**
- App Vivo: pra você fazer sua gestão
- O App Vivo é um canal de relacionamento

**Exemplos Incorretos:**
- App da Vivo
- Vivo App
- Nosso app

#### **Dentro do App**
Quando a pessoa usuária já está no aplicativo, evitamos reforçar "no app Vivo", pois o contexto já deixa claro onde a ação ocorre.

**Exemplo Correto:**
- Você encontra mais detalhes sobre isso em Assinaturas

**Exemplo Incorreto:**
- Você encontra mais detalhes sobre isso aqui no App Vivo, na seção Assinaturas

---

### **Meu Vivo Empresas**

#### **Como a gente fala**
O nome correto do produto é **Meu Vivo Empresas**. A sigla **MVE** é comum internamente, mas não deve ser usada nas comunicações externas.

**Exemplo Correto:**
- Meu Vivo Empresas

**Exemplos Incorretos:**
- MVE
- Vivo Empresas
- Meu Vivo Empresa

#### **Dentro do App ou Site**
Assim como no App Vivo, evitamos repetir "no Meu Vivo Empresas" quando o usuário já está dentro do ambiente digital.

**Exemplo Correto:**
- Você encontra mais detalhes sobre isso em Gestão de Linhas

**Exemplo Incorreto:**
- Você encontra mais detalhes sobre isso aqui no Meu Vivo Empresas, na seção Gestão de Linhas

---

## **Serviços Vivo**

A **assinatura** é o modo como chamamos a contratação de um serviço. Para manter consistência e clareza, os nomes dos serviços devem ser utilizados exatamente como foram definidos pelo time de Branding e validados por **Content Ops**.

### **Regras básicas**

#### **Uso da palavra Vivo**
O **Vivinho** substitui "Vivo" em imagens e banners, mas em **textos** a palavra "Vivo" deve ser escrita por extenso.

**Exemplos Corretos:**
- Vivo Controle
- Vivo Selfie
- Vivo Play
- Vivo Valoriza

**Exemplos Incorretos:**
- Controle
- Vivo selfie
- vivo Play
- Valoriza

#### **Uso de letras maiúsculas**
Os nomes dos serviços são **nomes próprios** e devem sempre começar com a primeira letra maiúscula.

**Exemplos Corretos:**
- Vivo Money
- Vivo Easy
- Vivo Controle

**Exemplos Incorretos:**
- Vivo money
- VIVO EASY
- Controle
- vivo Money

**Observação:** Quando os mesmos termos são usados como substantivos ou adjetivos, eles seguem a grafia normal.

**Exemplo Correto:**
- Na Vivo, você encontra tudo o que precisa para deixar sua casa inteligente.

**Exemplo Incorreto:**
- Acompanhe sua casa onde estiver com Casa Inteligente.

#### **Concordância nominal**
Os serviços Vivo podem ter **gêneros diferentes**. Antes de escrever, analise o contexto da assinatura:

**Exemplo Correto:**
- O **(plano)** Vivo Controle
- A **(co-marca)** Energia V

#### **Uso de estrangeirismos**
Os nomes de serviços podem conter palavras em inglês, mas evitamos adicionar **outros estrangeirismos** para manter a acessibilidade e compreensão.

**Exemplo:**
- Vivo Play (correto)
- Streaming Vivo Play (evite "streaming" se puder ser explicado de outra forma)

#### **Exceções**
- No **App Vivo**, já adotamos "Assinaturas" em vez de "Planos".
- No **B2B**, a mudança para "Assinaturas" ainda não tem previsão.

---

## **Serviços B2C**

### **Telefone Fixo ou Móvel**
- Vivo Controle
- Vivo Pré
- Vivo Pós
- Vivo Easy
- Vivo Família
- Vivo Selfie
- Vivo Total
- Vivo Travel

**Variações permitidas:**
- Vivo Selfie Globoplay
- Vivo Turbo
- Vivo Easy Prime

**Grafia correta:**
**Exemplo Correto:**
- Plano pré-pago
- Vivo Pós Família

**Exemplo Incorreto:**
- Plano Pré-Pago
- Plano pré pago
- Plano pré (sem "pago")

### **Para Casa e Bens**
- Vivo Casa Inteligente
- Vivo Fibra
- Vivo Guru
- Vivo Play
- Vivo Pets
- Vivo Seguros

### **Serviços Financeiros**
- Vivo Money
- Vivo Pay

### **Serviços de Uso Pessoal**
- Vivo Shopping
- Vivo Sustentável
- Vivo Valoriza

---

## **Serviços B2B**

### **Telefonia e Internet**
- Vivo Box
- Vivo Internet
- Vivo Voz Negócio

### **Soluções Empresariais Vivo**
- Energia V
- Vivo M2M
- Vivo Vita
- Vivo Agro
- Vivo Saúde
- Vivo Startup
- Vivo Tecnologia
- Vivo Meu Negócio

### **Para Gestão de Negócios e Pessoas**
- Frota Inteligente
- Vivo Valoriza Empresas

### **Para Investimentos**
- Vivo Ventures

### **Para Compras**
- Vivo Escritório

**Confira contextualizações e aplicações em frases:** [Figma - Assinaturas Vivo](https://www.figma.com/file/66dB3sNogLQcI40SNWNiQv/Assinaturas---Vivaz?type=design&node-id=3-826&mode=design&t=fWHCfJMopDbtR2uL-0)

**Para mais detalhes sobre serviços B2B:** [SharePoint - Assinaturas Vivo](https://telefonicacorp.sharepoint.com/:b:/r/sites/DESIGNOPSECAREVIVO.TMBNL/Content-Design/SiteAssets/SitePages/Home/1-ASSINATURAS-OK.pdf?csf=1&web=1&e=qXIPme)

---

# Diretrizes de Estilo e Formatação

Este guia reúne as diretrizes de estilo e formatação para garantir consistência e clareza na comunicação da Vivo. Aqui você encontrará orientações sobre nomes próprios, pontuação, número, unidades de medida, endereços, listas, hashtags e muito mais.

---

##Diretrizes de Abreviações, abreviaturas e siglas

###Abreviações

Abreviações são a forma reduzida de uma palavra, desde que não prejudiquem o entendimento da mensagem. Em nossas telas, o uso de abreviações amplamente reconhecidas no dia a dia está permitido.

**Exemplos Corretos:**
- "Vamos tirar uma foto do seu rosto."

**Exemplos Incorretos:**
- "Vamos tirar uma fotografia do seu rosto."

###Abreviaturas

As abreviaturas são a representação de uma palavra por meio de sílabas ou letras. Nos conteúdos da Vivo, elas devem ser evitadas, pois podem prejudicar a compreensão e a legibilidade das telas. Sempre que possível, a interface deve ser ajustada para permitir o uso da palavra completa.

Além disso, abreviações comuns da internet, como "vc" (você) ou "pq" (porque), são proibidas, pois comprometem a experiência do usuário e não seguem o tom de voz da Vivo.

**Exemplo correto:**
- Número do pedido
- Valor da fatura
- Minutos disponíveis

**Exemplo incorreto:**
- Nº do pedido
- Val. da fatura
- Min. disponíveis

**Exceções**
Há alguns casos específicos em que abreviações podem ser usadas, desde que estejam padronizadas e amplamente reconhecidas pelos usuários:
- **Unidades de medida:** MB, GB, TB (quando referindo-se a dados móveis ou armazenamento).
- **Termos técnicos padronizados:** Wi-Fi, SMS, 4G, 5G.
- **Formatos exigidos por espaço limitado:** Exemplo: "R$ 9,90/mês" em um botão de assinatura, quando há restrição de caracteres.


###Siglas

As siglas são escritas sempre com maiúscula e sem pontos. Algumas siglas são muito populares e, algumas vezes, nem mesmo sabemos o que significa a sua forma sem redução. Nesses casos, como SMS, CPF, RG, CNPJ, CNH, é permitido o uso apenas da sigla dentro do fluxo.
**Exemplo correto:**
A solicitação será aberta para o CNPJ.
**Exemplo incorreto:**
A solicitação será aberta para o Cadastro Nacional de Pessoas Jurídicas.

**Exceções**
- Em alguns casos, havendo espaço suficiente em tela, vale trazer as palavras completas ao invés da redução em siglas. Por exemplo: sabemos que PcD é uma sigla comum, mas se não tivermos alguma limitação de caracteres, opte por escrever "Pessoa com deficiência".

- Em textos mais longos (como em FAQs), quando se menciona uma sigla pela primeira vez, o ideal é identificar o nome completo a que ela se refere e citá-la entre parênteses. Exemplo: Associação Brasileira de Normas Técnicas (ABNT).

- Se há alguma chance de a sigla não ser entendida, não use.

---

##Diretrizes de Datas e horas
O ideal é iniciar e terminar com o mesmo formato de dentro de uma jornada, pra pessoa usuária não ter que aprender outro formato enquanto está navegando. Consistência é essencial.

###Dia da semana
A gente pode escrever só o primeiro nome do dia ou completo, sempre em letras minúsculas (exceto no começo de frases). Não é permitido abreviar, nem escrever usando o número. 
**Exemplos corretos**
- Segunda
- Segunda-feira
- Seu celular chega na segunda
- Seu celular chega na segunda-feira
**Exemplos incorretos**
- Seg
- 2ª feira
- Seu celular chega na Segunda-feira
- Seu celular chega na seg

###Mês
Os nomes dos meses são sempre em caixa baixa, mas obedecem a regra de início de frase. Só que não podem ser abreviados dentro do texto, a não ser que sigam o formato de datas (com dia ou ano).
**Exemplos corretos**
- Sua conta de dezembro chegou
- Dezembro é um mês de festas
- Sua conta vence em 12/jul
**Exemplos incorretos**
- Sua conta de Dezembro chegou
- Sua conta do mês 12 chegou
- Sua conta de Dez chegou
- Sua conta vence em jul

###Formatos de data
A gente tem uma ampla quantidade de formatos permitidos. Isso porque temos muitas interfaces que podem ser legados, alimentadas automaticamente por API ou outras questões.
O mais importante, nesse caso, é manter a consistência. Se você começou um fluxo escrevendo "14/12", não altere para "14 de dezembro".

**Exemplos**

**Dia e mês**
- dd/mmm = 25/jul
- dd/mm = 25/07
- dd/mês = 25/julho
- dd de mês = 25 de julho

**Mês e ano**
- mm/aa = março/18
- mm/aaaa = março/2018
- mês de ano = março de 2018

**Dia, mês e ano**
- dd/mm/aa = 25/07/18
- dd/mm/aaaa = 25/07/2018
- dd de mês de ano = 25 de julho de 2018

**Dia da semana**
- Dia da semana (dd) = quinta-feira (25) ou quinta (25)
- Dia da semana, dd de mês = quinta-feira, 25 de julho ou quinta, 25 de julho
- Dia da semana, dd de mês de ano = quinta-feira, 25 de julho de 2018 ou quinta, 25 de julho de 2018

**Observações**
- A gente tem uma ampla quantidade de formatos permitidos. Isso porque temos muitas interfaces que podem ser legados, alimentadas automaticamente por API ou outras questões.
O mais importante, nesse caso, é manter a consistência.

###Hora
O nosso padrão ao falar de horas e horários, é sempre com 2 algarismos, mas podemos usar 1 só quando tivermos problema de limite de caracteres. O formato de hora é de 00h a 23h e a abreviação de hora é sempre com a letra h em minúsculo. Pode até usar dois pontos ":" para separar hora de minuto, mas por questões de legibilidade, dê preferência pelo uso do "h". Pode contextualizar como horário da manhã quando a hora for menor que 13h. Não é preciso marcar os minutos com a letra m. Evite também trazer a abreviação "min". Quando formos citar um período de horas, devemos usar a crase em "às".

**Exemplo:**
- 9h30 da manhã

**Exemplos corretos**
- 00h
- 1h
- 9h01
- 09 horas
- 09 horas da manhã
- 14h15
- Aguarde 1 hora pra repetir a ação
- Aguarde 5 minutos e reinicie o celular
- Atendimento Vivo: 08h30 às 20h30

**Exemplos incorretos**
- 2hs
- 9h20
- 12h00
- 10hrs
- 10h50m
- 10h50min
- Aguarde 5 min e reinicie o celular
- Atendimento Vivo: 08h30 as 20h30

###Períodos de tempo
Em alguns casos, precisamos informar pra pessoa usuária quanto tempo vai demorar até a próxima ação: uma aprovação de pagamento, a resposta de uma solicitação, dentre outros casos.
Use a palavra "até" como apoio caso seja algo que possa se resolver antes do prazo e quando o período de tempo for em dias, é sempre importante destacar se são dias úteis. Caso sejam dias corridos, basta informar a quantidade.

**Exemplos corretos**
Até 5 dias
2 dias úteis

Quando o período de tempo for em horas, precisamos ter o cuidado de diminuir o esforço cognitivo. Períodos de até 48 horas podem ser sinalizados nesse tipo de unidade. Acima de 48 horas, passamos a contagem pra dias.

**Exemplos corretos**
Até 24 horas
Até 5 dias úteis 

**Exemplos incorretos**
120horas
até 72 horas

Caso você queira mencionar um período de um dia a outro, use a preposição "a". O travessão não deve ser usado por questões de acessibilidade e uso de leitor de tela

**Exemplo correto**
- 25/02 a 24/03

** Exemplo incorreto**
- 25/02 – 24/03

---

##Direrizes Endereços eletrônicos

###E-mails
São sempre escritos em letra minúscula.

**Exemplo correto**
A estrutura é padrão: js1190@terra.com.br
- Local-part: js1190
- Domínio: @terra
- Tipo de serviço: .com
- País: .br

E-mails que terminam no tipo de serviço (.com) são de domínios estadunidenses e não precisam de identificação de país. Quando o local-part for um nome que não identifica uma pessoa, serviço ou empresa, a gente coloca o nome no final, separado por hífen.


###Sites
Os endereços de sites são sempre em letras minúsculas e elementos mais técnicos do endereço, como HTTPS e www, não precisam aparecer.

**Exemplos corretos**
- vivo.com.br
- vivo.com.br/prepago

**Exemplos incorretos**
- https://www.vivo.com.br
- www.vivo.com.br
- Vivo.com.br

Sites têm nomes próprios, então quando precisar mencioná-lo junto ao endereço, tem que começar o nome com letra maiúscula (a não ser em casos como iPhone)

**Exemplos corretos**
- Vivo – vivo.com.br
- Wayra – br.pt.wayra.co

*Exemplos incorretos**
- vivo – vivo.com.br
- wayra – br.pt.wayra.co

###Extensão e extensões de arquivos
Pode ser tanto em maiúsculas, quanto em minúsculas, mas precisa estar contextualizado. Extensões de arquivos são jargões tecnológicos (siglas) e nem todo mundo precisa saber o que a sigla significa.
As extensões também são conhecidas por começarem com um ponto – então você pode escolher usar ou não.

**Exemplos corretos**
- Arquivo de Excel (.xlsx)
- Arquivo de Excel (xlsx)
- Arquivo PDF ou pdf
- Extensão PDF ou pdf
- Planilha do Excel (.xlsx)

**Exemplos incorretos**
- .xlsx (sem contexto)
- Arquivo .Xlsl
- Xlsl
- xlsx
- Portable document format

---

##Diretrizes de Formatação

A formatação deve seguir, prioritariamente, o Design System vigente.
Em caso de dúvidas, o recomendado é consultar a documentação do Mística no BrandFactory ou no Design System de MVE.

###Negrito
Aplicação permitida em palavras que mereçam destaque dentro de um bloco de texto, sempre com cuidado para não comprometer leiturabilidade, escaneabilidade, nem mesmo o peso de relevância da informação.
É necessário atenção para que o negrito não se confunda com um link em página. Por isso, o uso deve ser alinhado com UI Designer/Product Designer.

###Itálico
Não temos casos de uso previstos e não é necessário o uso de itálico para estrangeirismos ou jargões.

###Sublinhado
Por acessibilidade, só pode ser usado em casos que há um link inserido/embedado. Porém, em App Vivo não temos esse recurso. Nesse caso, links são sinalizados com bold e a cor púrpura.

###Tachado
Uso permitido pra mostrar que o texto foi corrigido ou que aquele termo está cancelado, como em casos de promoções, em que corrigimos um preço de/por.

###Alinhamento do texto
Os alinhamentos de texto devem seguir, prioritariamente, o Design System vigente Em caso de dúvidas, o recomendado é consultar a documentação do Mística no BrandFactory ou no Design System de MVE.
A gente evita usar textos justificados pra não acontecer aqueles espaços diferentes entre as palavras, nem passar a sensação de textos em blocos.
Cuidado apenas pra não deixar viúvas, ou seja, quando a palavra fica sozinha na última linha do texto. 

**Alinhado à esquerda**
Nossa recomendação é que, sempre que possível, os textos estejam alinhados à esquerda, pois facilita a leitura e aumenta o grau de escaneabilidade do conteúdo.
Cuidado apenas pra não deixar viúvas, ou seja, quando a palavra fica sozinha na última linha do texto.

**Alinhado à direita**
Pode usar, dependendo da situação. Geralmente é pra: Listas, textos curtos que precisam de destaque e ficar com o alinhamento igual ao de outros elementos na tela 

**Centralizado**
A gente usa menos que os outros. Isso porque, ao ler um conteúdo alinhado ao centro, nossos olhos precisam digitalizar os dois lados do texto e leva mais tempo do que ler o texto alinhado à esquerda, pois temos que encontrar onde a próxima linha começa. 
Caso precise aplicar, é recomendável apenas para títulos e textos muito curtos, com no máximo 2 linhas de comprimento.

---

##Diretrizes de Localizações e endereços

###Cidades
Nome de cidade é escrito por inteiro, sem abreviações. Quando o contexto não mostrar em que estado ela fica, é obrigatório trazer a localização completa, com as siglas referentes ao estado.

**Exemplos corretos**
- Osasco – SP
- Osasco (SP)

**Exemplos incorretos**
- Osasco – São Paulo
- Osasco – S.P.
- Osasco, São Paulo
- Osasco; São Paulo
- Osasco, S. Paulo
- Osasco (São Paulo)

###Estados
Quando estão sozinhos, podem aparecer tanto escritos por inteiro como abreviados.
Só precisa garantir que o usuário entendeu que aquele é um estado, principalmente quando tiver cidades com o mesmo nome, como São Paulo e Rio de Janeiro.

**Exemplos corretos**
- Estado de São Paulo
- Minas Gerais
- SP
- (SP)

**Exemplos incorretos**
- São Paulo
- Estado de S. P.
- Estado de SP
- M.G

###Países
A gente usa o nome completo do país.
**Exceção**
Devemos usar a sigla apenas como exceção.

**Exemplos corretos**
- África do Sul
- Alemanha
- Argentina

**Exemplos incorretos**
- Af. do Sul
- DEU
- ARG

###Endereços físicos
Os endereços físicos são compostos por:

**Tipo de endereço**
A gente dá preferência pelo nome completo do tipo de endereço. Se for extremamente necessário abreviar, é necessário que venha com dois pontos em seguida. Usammos Avenida, Rua, Praça, Alameda, Estrada, entre outros.

**Nome, número e endereço**
O indicado é não abreviar pra garantir que leitores de tela não façam confusão com nomes como General (Gal.) ou Santa (Sta.), mas há condições pra isso:
- É preciso ver se o endereço completo cabe na interface

Pra separar nome de número é só usar a vírgula e o número é sempre só com os algarismos (não precisa colocar “nº”). Quando o local for sem número, pode colocar “sem número”. A abreviação “s/n” deve ser evitada por questões de acessibilidade.

**Complemento de endereço**
O complemento deve ser uma área de preenchimento opcional. É separado por vírgula do nome e número. Também devem ser evitadas abreviações como apto. para apartamento, bl para bloco etc.

**Bairro**
Não se abrevia e é separado por hífen e espaço das outras partes do endereço.

**Cidade e Estado**
Sempre aparecem juntos, separados pela barra, e depois do Bairro. Também devem ser separados de outras partes com o hífen e espaço. A cidade não se abrevia e o estado é sempre com a sigla em 02 letras maiúsculas.

**CEP**
Segue o padrão, com 8 dígitos, sempre no formato: 99999-999

**Exemplos corretos**
- Rua Santa Rita de Cássia, 190 – Bairro – Cidade/SP – 99999-999
- R: Santa Rita de Cássia, 190 – Bairro – Cidade/SP – 99999-999
- Avenida Chucri Zaidan, sem número, apartamento 32 – Bairro – Cidade/SP – 99999-999

**Exemplos incorretos**
- R. Sta Rita de Cássia, 190 – Bairro – Cidade/SP – 99999-999
- Rua Santa Rita de Cássia 190 Bairro – Cidade/SP – 99999999
- Av. Chucri, s/n – Bairro – Cidade/SP – 99999-999

---

##Números
A gente prioriza o algarismo. É mais fácil de ler e chama atenção quando está dentro do texto.

###Números gerais
Só precisa tomar cuidado com o 0 (zero), pois ele é parecido com a letra "o" em maiúscula. Quando ele aparece sozinho, a gente faz o teste de qual formato é melhor: zero ou 0.
Em casos de números no feminino, nós usamos por extenso: uma, duas etc.

**Exemplos corretos**
- Vamos enviar a resposta em até 2 dias úteis
- Você tem uma fatura

**Exemplos incorretos**
- Vamos enviar a resposta em até dois dias úteis
- Você tem 1 fatura

**Exceções**
-Alguns números podem ser escritos por extenso ao invés dos algarismos, pra facilitar a leitura. 
**Exemplos corretos**
- 2 mil
- 1 milhão
- 2 milhões
- 10 milhões
- 1 bilhão

-Em textos jurídicos e apenas em textos jurídicos, também é recomendado trazer tanto o algarismo quanto o texto escrito.
**Exemplos corretos**
- Prazo de 2 (dois) dias úteis
- O serviço será concluído em 2 (duas) horas
- 12 (doze)
- 23 (vinte três)
- 50 (cinquenta)
**Exemplos incorretos**
- DOZE meses
- 12 meses

##Ordinais
- Por acessibilidade, vamos priorizar a escrita por extenso: primeiro, primeira. Isso porque alguns leitores de tela não conseguem fazer a leitura correta do caractere e dão como retorno "1 ordinal feminino", por exemplo.
Caso tenhamos algum problema relacionado a espaço disponível pro texto ou quantidade de caracteres, é permitido o uso da grafia com símbolo. Nesse caso, o caractere precisa estar sempre junto ao número: 1º, 1ª.

**Exemplos corretos**
- 1ª parcela em dia
- 10ª parcela em dia
- Primeira parcela em dia
- Parcela 11 em dia

###Decimais
Casa decimal é sempre com vírgula. Ponto é pra separar milhar.
**Exemplos corretos**
- 4,5 GB
**Exemplos incorretos**
- 4.5 GB

###Frações
O mais recomendado é evitar escrevermos frações de forma geral, em especial com numerais, porque pode ser confundido com datas.
Caso seja necessário e for sobre as medidas mais conhecidas, é melhor colocar o texto por escrito.
**Exemplos corretos**
- Passo 1 de 12
- Meio
**Exemplos incorretos**
- 1/12
- ½

###Porcentagem
Devemos usar o símbolo de porcentagem junto dos números.
**Exemplos corretos**
- 10%
**Exemplos incorretos**
- 10 %

**Exceção**
Em textos jurídicos, é comum escrevermos por extenso. Nesse caso, não é permitido misturar texto escrito com símbolo.
**Exemplos corretos**
- Vinte por cento
- 20 (vinte) por centro
**Exemplos incorretos**
- Vinte %

###Valores e Dinheiro
As regras são simples:
	
- Use o símbolo da moeda, no caso do Brasil, o real: R$
- Sempre use espaço entre símbolo e o número: R$ 2
- Milhar é separado por ponto: R$ 1.250
- É possível abreviar em caso de números redondos: R$ 5 mil
- Nunca quebrar a linha no meio do valor. Tem que aparecer sempre por inteiro: R$ 25,14
- É regra que no caso de valores arredondados, em que não há centavos, vamos sempre escrever sem o uso de casas decimais: R$ 2.
- Quando houver quebra em centavos, trazemos a casa decimal, sempre separada por vírgula: R$ 2,50

**Exemplos corretos**
R$ 122/mês

**Exemplos incorretos**
R$ 122,00/mês

**Exceções**
Nos casos de promoções e ofertas, é comum encontrarmos os números tachados. Porém, leitores de tela não fazem a diferenciação do tachado e, com isso, não indicam para as pessoas que fazem uso dessa tecnologia de que esse é o preço antigo. Por isso, a recomendação é de sempre usarmos os textos "De/Por" acompanhados dos valores. Caso não seja possível acrescentar na interface o "De/Por", deve ser adicionado como literal na spec.
**Exemplo correto**
De R$ 2.310,50 Por R$ 2.199,50


###Idade
Se precisar falar da idade, a gente só menciona o número e a palavra "anos. Nunca falamos se alguém é jovem, criança, idoso, adulto, etc.
**Exemplos corretos**
- 18 anos
- 30 anos

---

##Diretrizes de Números de telefone
O padrão é com 3 elementos: DDD + prefixo + sufixo.
###Fixo e celular
O padrão é com 3 elementos: DDD + prefixo + sufixo. Quando precisar identificar o país, daí tem 4 elementos: código do país + DDD + prefixo + sufixo. Em ambos os casos, prefixo e sufixo são sempre separados por hífen.

**Exemplos corretos**
- (11) 91234-5678
- (11) 1234-5678
- +55 (11) 91234-5678
**Exemplos incorretos**
- 1191234-5678
-  912-345-678
- 1234-5678
- 91234-5678

###Com código da operadora
Quando for necessário citar o código da operadora, sempre usamos o 15.
**Exemplo correto**
(+15 + DDD) + prefixo + sufixo

Em casos que o espaço para descrição do telefone é amplo, pode-se utilizar o zero, o termo “operadora” e o código do DDD:
**Exemplo correto**
(0 + operadora + DDD) + prefixo + sufixo

Quando há limite de caracteres, esse é o formato indicado:
**Exemplo correto**
(0xxDDD) + prefixo + sufixo 

###Outros telefones
Também precisam ser apresentados por completo, como números com 0800 ou número reduzido. Nesses casos, evitamos a separação por hífen.
**Exeplos corretos**
- 0800 123 4567
- 103 15
- *8416
**Exemplos incorretos**
- 0800-123-4567
- 103-15

---

##Diretrizes de Pontuação, pontuações e símbolos

###Ponto final
Usamos apenas como ponto simples entre frases. Não usamos como ponto final.
**Exemplos corretos**
Você negociou suas faturas
**Exemplos incorretos**
Você negociou suas faturas.

###Vírgulas
A recomendação é seguir as regras da Língua Portuguesa. Aqui temos algumas possibilidades de uso da vírgula.
- Separar elementos em enumerações e repetições
- Isolar o adjunto adverbial
- Isolar expressões
- Isolar advérbios “sim” e “não” em respostas
- Isolar o nome do lugar numa data
- Suprimir uma palavra
- Separar orações ligadas ou não por conjunções
- Separar orações intercaladas
- Separar orações adverbiais
**Recomendação**
Separar sujeito de verbo é um dos casos mais comuns e também mais graves. Tem 2 casos onde se pode fazer isso, que é com o aposto ou com o vocativo.

###Ponto e vírgula ou ponto vírgula
A gente pode usar quando for separar os itens de uma lista, dependendo da formatação. Se a lista não tem algo que mostra que é uma lista, como algum símbolo antes de cada item, a gente usa o ponto e vírgula pra mostrar que é uma lista.
**Exemplos**
- Item1;
- Item 2;
- Item 3;
**Recomendação**
Agora, se a lista tem esses símbolos marcando cada item nem precisa do ponto e vírgula ao final (ou então fica visualmente carregado). 
•	Item 1
•	Item 2
•	Item 3

###Dois pontos
É o ponto que vem antes de mostrar algo. Sabe quando a gente dá uma pausa antes de falar um exemplo ou uma lista pra alguém? É isso.
O bom dos dois pontos é que ele indica que o texto continua, com um pouco mais de ênfase que um ponto ou uma vírgula.
Depois dos dois pontos, o texto começa sempre com inicial minúscula (a não ser quando for um nome próprio).

###Uso de Barra e Barra oblíqua
A barra sempre deve ser usada sem espaçamento entre palavras ou números.
**Exemplos corretos**
- Datas: 01/jan
- Pra mostrar períodos seguidos: janeiro/fevereiro
- Relações entre partes: singular/plural, km/h
- Pra substituir o “ou”: 2G/3G/4G
- Pra usar “e/ou"
- Pra sinalizar recorrência: R$29,00/mês

###Hífen
Para o uso do hífen, basta seguir as regras da Língua Portuguesa. Aqui temos algumas possibilidades de uso do hífen.
- Separação de substantivos compostos
- Separação de substantivos acompanhandos dos advérbios “mal” e “bem”
- Separação de substantivos acompanhandos das palavras “além”, “aquém”, “recém” e “sem”

###Exclamação
Evitamos o uso excessivo de pontos de exclamação e nunca usamos mais de um ponto de exclamação, seja na mesma frase, seja em sequência. Quando formos usar, devemos tomar cuidado apenas para não tornar a frase imperativa, como se estivéssemos brigando com a pessoa usuária ou a obrigando a tomar alguma ação.
***Exemplo correto**
- Você contratou a Vivo Fibra. Aproveite seu novo plano!
**Exemplo incorreto*
- Você contratou a Vivo Fibra! Aproveite seu novo plano!
- Você contratou a Vivo Fibra. Aproveite seu novo plano!!!


###Interrogação 
Usamos quando queremos fazer, de forma direta, uma pergunta para a pessoa usuária. Vale destacar que evitamos iniciar diálogos com perguntas fechadas (respostas sim e não).
**Exemplo correto**
Em qual linha você quer fazer a recarga?

###Parênteses
Preferimos não usar parênteses, mas ele não é proibido. Podemos usá-los em textos jurídicos, onde precisamos escrever números por extenso, e ao apresentar siglas.
**Exemplos corretos**
- O prazo é de 24 (vinte e quatro) horas
- Regulamentado pela Agência Nacional de Telecomunicações (Anatel)

###Reticências
Preferimos por não usar reticências, mas não é proibida. Como ela é usada pra mostrar que algo não foi dito ou terminado na frase, pode ser entendida como uma frase inacabada e confundir a pessoa usuária. É preciso ter atenção para que não passe uma ideia incompleta ou insegurança.

###Arroba
Pode ser usado em dois casos: dentro do formato de e-mail e pra identificar a pessoa usuária de rede social.
**Exemplos**
- nome.sobrenome@telefonica.com
- Instagram: @vivo

###Asterisco
O uso de asterisco deve ser evitado. Muita gente já imagina que o fato de ter um asterisco quer dizer que tem mais informação sobre o que está escrito, mas que não está aparecendo ali. Isso reforça a ideia de que estamos escondendo a informação, o que vai contra o nosso DNA Vivo.

###Aspas
É preciso analisar a real necessidade do uso de aspas, pois o texto pode ficar carregado tanto visualmente quanto pra leitores de tela. Para sinalizar uma seção, por exemplo, podemos apenas usar a inicial maiúscula. Se, ainda assim, for muito importante, optamos pelo uso de aspas duplas.

---

##Diretrizes de Bytes e bits
É preciso ter bastante atenção, porque existe uma diferença entre bytes e bits. Para nos referirmos à velocidade da nossa internet, vamos priorizar o uso de bytes. O certo é escrever o número separado da sigla ou abreviação, pra que os leitores de tela não tenham problema na hora da leitura. Além disso, separamos casas decimais por vírgulas.

###Internet Fibra
Usaremos sempre as palavras por extenso, no singular, com apenas a primeira letra em caixa alta.
**Exemplos corretos**
- Mega
- Giga
- 100 Mega
- 1Giga
**Exemplos incorretos**
- Megas / Gigas
- mega / giga
- MEGA / GIGA
- 100 mega / 100 MEGA

###Internet Móvel
Usamos apenas a sigla, totalmente em caixa alta.
**Exemplos incorretos**
- MB
- GB
- 50 MB
- 1,44 MB 
- 3 GB
**Exemplos incorretos**
- mb / gb
- 50 mg / 3 gb
- 1.44 MB / 1.44 mb

###Byte
Byte (símbolo "B") é a unidade geralmente usada para determinar espaço de armazenamento e quantidade de memória RAM. São sempre escritos com letras maiúsculas.
**Exemplos**
- B = byte
- KB = kilobyte
- MB = megabyte
- GB = gigabyte
- TB = terabyte

###Bit
Bit (símbolo “b”) é a menor unidade usada para medir a transferência ou armazenamento de informação digital. São sempre escritos com letras minúsculas.
**Exemplos**
- b = bit
- kb = kilobit
- mb = megabit
- gb = gigabit
- tb = terabit

###Transferência de dados
Quando tratamos sobre transferência de dados, ou seja, sobre velocidades de download e upload, temos que fazer uma combinação de unidade de medida sobre unidade de tempo.
**Exemplos**
- Kbps = quilobits por segundo
- Mbps = megabits por segundo

---

##Diretrizes de Emojis e emoticons
É importante entendermos a diferença entre emoticons e emojis. Por acessibilidade, não é permitido o uso de emoticons, como :) ou ;). Já os emojis, como 😄, podem ser usados, mas com algumas condições.
Os emoticons são proibidos porque são lidos por alguns leitores de tela apenas como pontuação, ou até mesmo como erros gramaticais ou de digitação. 
O emoticon rosto feliz :) pode ser lido como "dois pontos parênteses" – o que não passa a mensagem que gostaríamos.
Já os emojis podem ser usados, sempre com cuidado. Não esqueça que emojis tem texto alternativo embedado, então tenha empatia com nossas pessoas usuárias que precisam fazer uso de leitores de tela.
Precisamos evitar uma sobrecarga de imagens dentro das nossas telas. Se estiver em uma jornada com muitos botões, fotos e ícones, opte por não usar o emoji.

###Boas práticas para uso de emojis
**Jamais use um emoji para substituir uma palavra** - Emojis podem deixar a jornada mais leve e divertida, mas quando usados substituindo uma palavra, podem mudar completamente a mensagem, bem como aumentar excessivamente a carga cognitiva da pessoa usuária.
**Evite o excesso de emojis** - Em uma mesma mensagem, o ideal é fazer o uso de apenas um emoji. Se usamos "Hoje tem festa 🎈🎈🎈", um leitor de tela leria como "Hoje tem festa balão balão balão". Ou seja, deixamos nossa mensagem repetitiva, carregada e cansativa para quem usa esse recurso de leitura.
**Emojis sempre vem no final da mensagem** - Emojis não devem ser usados como ícones e, por isso, os textos são sempre prioritários. As pessoas usuárias precisam entender a mensagem primeiro, depois colocamos os acessórios.
**Use emojis amplamente conhecidos** - Não use emojis pouco conhecidos ou que abram interpretações ambíguas, aumentando a carga cognitiva. Interpretação é algo muito pessoal e, ao ver um emoji, uma pessoa pode entender algo completamente diferente do que você quis passar.
**Cuidado com o contraste de cores** - A regra de cores para acessibilidade também deve ser aplicada ao uso de emojis. Por isso, ao escolher, não esqueça de conferir se há contraste o suficiente, seja com fundos claros, seja com fundos escuros.
**Emojis de partes do corpo devem sempre ser em amarelo** - O amarelo é considerado o tom mais neutro de pele. Por esse motivo, sempre que tiver que usar um emoji de rostos, mãos ou qualquer outra parte do corpo, use essa opção.

---

##Diretrizes de Jargões, gírias e estrangeirismo
Use com cuidado.

###Jargões
Temos muitos jargões no universo de telecomunicações e devemos evitá-los ao máximo. Quando for indispensável o uso, tente trazer algum texto explicativo de apoio ou deixe o fluxo o mais simples possível para evitar a frustração da pessoa usuária.
Tenha sempre em mente que, por aqui, prezamos pela linguagem simples e pela comunicação inclusiva.
Fale a expressão para, pelo menos, 5 pessoas de diferentes lugares e contextos (idade, classe social etc.). Se uma delas não entendeu ou interpretou de forma diferente, o ideal é não utilizar.
**Exemplo correto**
- Você pode entrar em contato pela internet do seu celular.
**Exemplo incorreto**
- Você pode ativar o 3G do seu smartphone e entrar em contato pela web.

###Gírias
Gírias e termos populares nos meios digitais fazem parte da nossa identidade verbal. No entanto, somos uma marca que conversa com uma diversidade de pessoas, então, na hora de usar gírias, leve sempre em consideração se elas fazem sentido quanto a idade, regionalidade e público-alvo da mensagem.
**Exceções**
-Somos uma marca atual, atenta às tendências e ao que acontece no universo digital. Se for usar memes ou gírias na comunicação, avalie se ainda são novidade, se não foram utilizados em excesso pelas pessoas e se estão acessíveis a todos, e não a um grupo específico – a não ser que este seja o objetivo.
-Não use gírias nos fluxos de atendimento ao cliente, principalmente os que possam ter contextos críticos (como cancelamentos), para evitar qualquer tipo de mal-entendido.
Em caso de dúvida, consulte o time de Content Design Ops ou as pessoas UX Writers alocadas nas squads de App Vivo e MVE.

###Estrangeirismo
Sempre que possível, vamos evitar o uso de estrangeirismos, para conseguirmos simplificar a nossa linguagem e atender aos direcionamentos de tom e voz da Vivo.

Quando for inevitável, considere acrescentar, em algum momento, uma tradução ou explicação do que significa e preencha a documentação de Acessibilidade, com a marcação de inclusão de tag lang para que tecnologias assistivas façam a leitura no idioma correto. Em caso de dúvidas, acesse o Framework de Acessibilidade. 
**Exemplo correto**
-  40% de cashback, ou seja, seu dinheiro de volta
 
---

##Diretrizes de Maiúsculas e minúsculas
É preciso ter atenção ao uso excessivo de letras maiúsculas nos textos, letras maiúsculas são usadas apenas pra:
- início de frases; 
- início de palavras em itens dentro de uma lista; 
- primeira palavra de um título ou botão; 
- nomes próprios; nomes comerciais (marcas, produtos); 
- nomes de seções e rótulos de seções (que se referenciadas em outras páginas, também aparecem com letra maiúscula para orientar a pessoa usuária sobre qual página/área/seção estamos falando); 
- nomes de países, estados, cidades, bairros, regiões; 
- abreviaturas e siglas.

Não usamos textos inteiros em caixa alta, porque isso foge da nossa proposta de textos amigáveis. Afinal, na internet, escrever totalmente com letras maiúsculas passa a impressão de que estamos gritando com a pessoa usuária.

**Exceções**
A única exceção em que é permitido o uso de caixa alta são nos títulos de seção, rótulos de seção ou em marcas cuja grafia já seja assim.

---

##Diretrizes de Nomes próprios e marcas
Nomes próprios começam sempre com a inicial maiúscula, seja pra nomes de pessoas, seja pra lugares. No caso das marcas e empresas, precisamos respeitar a grafia de acordo com os guias de cada empresa. A maioria segue a regra apenas da primeira letra em maiúscula, mas temos exemplos como iPhone, iPad e WhatsApp.
Em caso de dúvida, acesse o site oficial da empresa que deseja mencionar e consulte a grafia aplicada em algum texto.

**Exemplo correto**
- Microsoft
**Exemplo incorreto**
- MICROSOFT

---

##Diretrizes de Unidades de medida
Pode usar de dois jeitos: tanto por escrito quanto abreviado. Vale apenas se certificar de que o uso da abreviação não prejudica o entendimento do que está sendo informado. Ao usar uma unidade de medida, sempre dê espaço entre o número e a unidade. No caso de abreviação, esta deve sempre estar em letras minúsculas.
Também é preciso atenção com o uso de casas decimais, que devem ser separadas com vírgula.
**Exemplos corretos**
- 10 centímetros ou 10cm
- 10 metros ou 10m
- 10 quilômetros ou 10km
1,6 quilogramas ou 1,6kg
**Exemplos incorretos**
- 10cm
- 10 kilômetros
- 1,6 kilogramas
- 1,6 KG

---

##Diretrizes de Listas
A lista é um recurso que deve ser utilizado para exibir um conteúdo mais focado, de fácil leitura e organizado
- Termine com dois pontos a frase anterior ao início da lista
- Comece as frases sempre com letras maiúsculas
- Tente usar a construção paralela como recurso. Se um item começa com um verbo, os demais itens devem começar com um verbo
- Priorize o uso para informações mais simples e curtas, evitando mais de 5 itens
- Não use pontuação ao final das frases, exceto se forem perguntas
- Não use “e”, “ou” ou “e/ou” no início de qualquer item da lista
- Evite ter mais de uma lista com marcadores em uma tela

###Lista com marcadores (bullet points)
Use para uma lista com itens relacioandos, que não precisam estar em uma ordem específica

###Lista numerada
Use para uma lista que precisa ter uma ordem específica em que as aões devem ocorrer por grau de importância, como em um passo a passo de como navegar por uma área.

**Exceções de pontuação**
A gente pode usar quando for separar os itens de uma lista, dependendo da formatação. Se a lista não tem algo que mostra que é uma lista, como algum símbolo antes de cada item, a gente usa o ponto e vírgula pra mostrar que é uma lista.
**Exemplos**
- Item1;
- Item 2;
- Item 3;
**Recomendação**
Agora, se a lista tem símbolos marcando, como hífen e ponto lista, os itens não precisam do ponto e vírgula ao final (ou então fica visualmente carregado). 
•	Item 1
•	Item 2
•	Item 3
---

##Diretrizes de Hashtags
Na nossa comunicação, usamos hashtags como ferramenta e não apenas como um elemento visual ou assinatura. As hashtags são de uso específicos em campanhas que tenham o objetivo de levar à ação, como promoções e prêmios; em conteúdos que tenham o objetivo de alcançar maior visibilidade; em publicações que tenham o objetivo de fazer parte de um movimento ou ação.
A grafia é sempre com a primeira letra de cada palavra em maiúsculo. Assim, facilitamos a leitura. No caso de hashtags com palavras acentuadas, a recomendação é manter o acento. Também usamos Vivo sempre como nome, nunca como verbo.
**Exemplos corretos**
- #FuturoVivo
- #VivoSustentável
- #VivoMais
- #Vivo5G
- #TemVivoPraTudo
- #VemPraVivo
**Exemplos incorretos**
- Hashtags extensas: #TodoMundoCurteAVivo
- Hashtags como assinatura de campanha
- Hashtags em excesso e semelhantes na mesma mensagem

---

# Diretrizes de Acessibilidade na Vivo

Este guia reúne as diretrizes e boas práticas de acessibilidade na Vivo, alinhadas aos padrões internacionais (WCAG) e regulatórios (MORGA). Nosso objetivo é garantir que todos os produtos e serviços sejam acessíveis e inclusivos, proporcionando uma experiência digital de qualidade para todas as pessoas.

---

## Acessibilidade em Conteúdo na Vivo
Nossas práticas são baseadas nos manuais internos da Vivo e nas diretrizes da **WCAG** e **MORGA**.

### Framework de Acessibilidade Vivo
O **Framework de Acessibilidade Vivo** é a ferramenta oficial para desenvolvimento de acessibilidade digital. Ele fornece guias e templates para cada etapa do projeto, desde o planejamento até o lançamento.  
- **Link**: [Framework de Acessibilidade Vivo](https://zeroheight.com/4e1de193d/p/960580-introducao)

### WCAG (Web Content Accessibility Guidelines)
Desenvolvido pela **W3C**, o WCAG é o principal documento internacional que define princípios, diretrizes e critérios de sucesso para acessibilidade na web.  
- **Princípios**: Perceptível, Operável, Compreensível e Robusto.

### MORGA (Manual Técnico-Operacional dos Procedimentos de Implantação do Regulamento Geral de Acessibilidade)
O **MORGA** é uma diretriz regulatória da **Anatel** que orienta a fiscalização e promove a acessibilidade no setor de telecomunicações.

---

## Princípios de Acessibilidade na Vivo
Nossas diretrizes seguem os 4 princípios da acessibilidade:

1. **Perceptível**:
   - As informações e componentes da interface devem ser apresentados de forma que todas as pessoas possam percebê-los.
   - **Exemplo**: Use texto alternativo em imagens e legendas em vídeos.

2. **Operável**:
   - A interface deve ser operável por todas as pessoas, independentemente de suas habilidades.
   - **Exemplo**: Garanta que todos os elementos interativos sejam acessíveis via teclado.

3. **Compreensível**:
   - As informações e operações da interface devem ser compreensíveis.
   - **Exemplo**: Use linguagem clara e evite jargões técnicos.

4. **Robusto**:
   - O conteúdo deve ser interpretável por uma ampla variedade de tecnologias, incluindo leitores de tela.
   - **Exemplo**: Utilize HTML semântico e ARIA para melhorar a compatibilidade.

---

## Sobre Diversidade na Vivo
A Vivo nasceu no Brasil e para as pessoas brasileiras. Nossa marca representa a pluralidade e a diversidade do país, com o objetivo de humanizar a tecnologia móvel.

### Representatividade e Inclusão
- **Diversidade de gênero, idade e cor**: Nossa comunicação reflete a pluralidade brasileira, quebrando estereótipos e promovendo representatividade.
- **Não à discriminação**: Não toleramos nenhum tipo de discriminação. Nossas diretrizes buscam eliminar discursos e atitudes que possam ofender ou deslegitimar qualquer pessoa ou grupo social.

---

## Sobre Inclusão na Vivo
Na Vivo, nossa missão é **Digitalizar para Aproximar**. Para isso, usamos uma linguagem inclusiva que respeita as diferentes culturas e identidades do Brasil.

### Linguagem Inclusiva
- **Respeito e dignidade**: Tratamos nossos clientes com respeito, usando palavras que promovem a inclusão.
- **Exemplos de práticas inclusivas**:
  - Evitar termos capacitistas, como "clique aqui" ou "veja mais".
  - Usar pronomes neutros ou adaptados ao contexto.
  - Garantir que o conteúdo seja acessível a pessoas com diferentes níveis de conhecimento.

---

## Boas Práticas de Acessibilidade em Conteúdo na Vivo

### Textos Acessíveis
Para cumprir os critérios de acessibilidade, diversidade e inclusão, siga as seguintes diretrizes:

#### Premissas de UX Writing
- **Clareza**: Use linguagem simples e direta.
- **Concisão**: Evite frases longas e informações desnecessárias.
- **Utilidade**: Forneça informações relevantes e úteis.
- **Consistência**: Mantenha padrões de voz, tom e estilo.
- **Acessibilidade**: Garanta que o conteúdo seja acessível a todos.

#### O que fazer:
- **Use linguagem simples**.
- **Dê instruções claras**.
- **Construa textos curtos**.

#### O que evitar:
- **Cacofonias**: Evite combinações de palavras que gerem sons desagradáveis (ex.: "fatura futura").
- **Jargões e termos complexos**: Explique termos técnicos quando necessário.
- **Sobrecarga de informações**: Evite encher uma tela com muitas informações.
- **Frases longas**: Priorize frases curtas e diretas.

### Verbos de Ação
- **Evite nominalizações**: Use verbos de ação para reduzir a carga cognitiva, principalmente para pessoas neurodivergentes.
- **Exemplos Corretos**:
  - "Pagar fatura."
  - "Agendar visita técnica."
- **Exemplos Incorretos**:
  - "Pagamento da fatura."
  - "Agendamento de visita técnica."

### Evite Termos Capacitistas ou Excludentes
- Evite expressões que possam excluir ou subestimar a experiência das Pessoas com Deficiência. Sempre use alternativas acessíveis aos verbos que impliquem sentidos físicos. Palavras associadas a sentidos específicos, como "ver", "ouvir", "falar" e "olhar" são proibidas e devem ser substituídas por termos que não evoquem capacidades físicas.
- **Exemplos Corretos**:
  - "Consultar o saldo"
  - "Conferir o e-mail"
  - "Ler o livro"
  - "Acessar a fatura"
  - "Assistir ao vídeo."
  - "Selecionar a opção desejada"
- **Exemplos Incorretos**:
  - "Ver o saldo"
  - "Clicar na opção desejada"
  - "Ficar de olho no vídeo."
  - "Tenha em mãos seus documentos."
  - "Dar um pulinho"
  - "Fale conosco"

### Priorize Frases Afirmativas
- Frases afirmativas ajudam a reduzir esforço cognitivo e tornam a mensagem mais clara.
- **Exemplos Corretos**:
  - "Tente de novo mais tarde."
- **Exemplos Incorretos**:
  - "Não vai dar pra fazer isso."

---

## Texto Alternativo em Imagens
O texto alternativo deve descrever a imagem de forma clara e concisa, seguindo estas diretrizes:

### Dicas Básicas:
- **Limite de caracteres**: Até 125 caracteres.
- **Estrutura**: Use a fórmula **sujeito + contexto + ação**.
- **Pontuação**: Siga as regras de ortografia e gramática.
- Não use "Imagem de...", pois leitores de tela já identificam esse formato.


### Observação:
- Você pode encontrar mais informações sobre imagens no nosso Guia de Acessibilidade em https://zeroheight.com/4e1de193d/p/0102bc-1-todas-as-imagens. 
- **Imagens decorativas**: Não é necessário descrever imagens que não agregam funcionalidade.

---

## Linkagens Contextualizadas
Os links devem indicar claramente o destino e a finalidade. Evite palavras genéricas.

### O que evitar:
- **"Clique aqui"**, **"Acesse aqui"**, **"Confira abaixo"**, **"Saiba mais"**, **"Ver mais"**.

**Exemplos Corretos:**
- Acesse a sua fatura
- Veja os detalhes do seu plano

**Exemplos Incorretos:**
- Clique aqui
- Saiba mais

**Observação*:
- Você pode encontrar mais informações sobre imagens no nosso em nosso Framework de Acessibilidade https://zeroheight.com/4e1de193d/p/330122-5links-fora-de-contexto.


---

## Como Abordamos Deficiências na Vivo
Sempre use o termo **Pessoa com Deficiência (PcD)**. Evite termos como "deficiente", "deficiente físico" ou "necessidades especiais". A sigla **PcD** sempre usa "c" minúsculo e não recebe "s" no plural.
Atendimento especializado deve focar na necessidade, e não na deficiência. Exemplo: **Atendimento em Libras**, e não "Atendimento para surdos".

### Tipos de Deficiências:
Deficiências podem ser **permanentes** (irreversíveis) ou **transitórias** (temporárias). Alguns subgrupos:
- **Física:** Tetraplegia, amputação de membros, paralisia cerebral.
- **Intelectual:** Dificuldades em raciocínio, aprendizado ou memória.
- **Auditiva:** Redução ou ausência de audição.
- **Visual:** Baixa visão ou cegueira.
- **Múltipla:** Combinação de duas ou mais deficiências.


---

## Gênero e Linguagem Inclusiva
Adotamos práticas de linguagem inclusiva para evitar a flexão de gênero e promover a neutralidade.

### Boas Práticas:
1. **Remova marcadores de gênero**:
-Artigos como "o/os" e "a/as" e pronomes como "nosso" e "nossa" são os que costumam marcar se estamos falando de pessoas do sexo feminino ou masculino. Para sermos mais neutros, podemos remover o uso dos artigos em alguns textos ou, até mesmo, optar pelo uso de artigos e pronomes indefinidos ou substituir os plurais que, comumente são termos masculinos, por outros mais genéricos.
   - **Exemplo Correto**: "Clientes Vivo vão ganhar bônus de internet!"
   - **Exemplo Incorreto**: "Os clientes Vivo vão ganhar bônus de internet!"

2. **Use “pessoas” para substantivos que variam de acordo com o gênero**:
- A palavra "pessoas" ajuda a neutralizar a carga de gênero que alguns substantivos, principalmente aqueles relacionados à profissões, costumam carregar.
   - **Exemplo Correto**: "Pessoas desenvolvedoras."
   - **Exemplo Incorreto**: "Os desenvolvedores / As desenvolvedoras."

3. **Evite caracteres especiais**:
-Apesar de ter se tornando popular, o uso de "x" ou "@" na grafia das palavras não é acessível. Isso porque torna a palavra impronunciável, principalmente para leitores de tela, e aumenta a carga cognitiva para pessoas neurodivergentes. Por isso, opte sempre pelo caminho de trocar por palavras mais neutras ou outras expressões, ao invés de usar caracteres especiais.
   - **Exemplo Correto**: "Boas-vindas ao Vivo App."
   - **Exemplo Incorreto**: "Bem-vind@ ao Vivo App."

---

## Mais sobre Pessoas e Acessibilidade Além da Deficiência
Acessibilidade, diversidade e inclusão não se limitam a pessoas com deficiência. Elas também contemplam:

- **Pessoas de baixa escolaridade**.
- **Pessoas idosas**.
- **Pessoas periféricas**.
- **Outros grupos e minorias**.

### Boas Práticas:
- **Idade**: Use a idade específica em algarismos (ex.: "19 anos"). Evite adjetivos como "velho" ou "novo".
- **Raça, cor e etnia**: Evite mencionar características físicas ou usar eufemismos racistas (ex.: "morena clara", "neguinho").

---


## **Padrões de Acessibilidade em Botões**
Para garantir **usabilidade e acessibilidade**, os botões seguem uma nomenclatura padronizada nas **specs de acessibilidade**.

**Regras para Identificação de Botões:**

- **Botão Voltar na Navbar** → Identificado apenas como **“Voltar”**.
  - Não usamos **“Voltar para tela anterior”** ou **“Voltar para o início”**.
  - Esse botão é padrão na **Navbar** e não pode ser alterado individualmente por restrições técnicas.

- **Botão Fechar em Alertas/Toast** → Identificado como **“Fechar alerta”**.
  - O leitor de tela interpreta toasts/notificações como alertas (sucesso, erro ou informação), exigindo essa nomenclatura.

- **Botão de Filtros** → Identificado como **“Escolher filtros”**.
  - Permite à pessoa usuária configurar filtros de busca.

- **Botão Fechar em Modais** → Identificado como **“Fechar janela”**.
  - Evitamos trazer contexto adicional para reduzir a carga cognitiva.

- **Botão Ajuda** → Identificado como **“Ajuda”**.
  - Representado por um **ícone de interrogação** no topo da tela.

- **Botão de Menu** → Identificado de duas formas:
  - No **App Atual**: **“Menu Mais”**.
  - No **Novo App**: **“Menu”**.

- **Botão de Perfil** → No **Novo App**, identificado como **“Perfil”**.

---

# Diretrizes e Padrões de Conteúdo nas Interfaces da Vivo

Este guia reúne as diretrizes e padrões para criação de conteúdo nas interfaces da Vivo, garantindo consistência, clareza e alinhamento com a identidade da marca. Aqui você encontrará orientações sobre aceite de termos, botões, entrypoints e muito mais.

---

## Aceite de Termos e Condições de Uso
Serve para informar à pessoa usuária sobre termos e condições obrigatórias que ela precisa aceitar antes de continuar a jornada.

São mensagens obrigatórias ao longo da experiência, determinadas por instruções do jurídico e aprovadas por Content Ops. 

Para o **Novo App Vivo**, a opção de checkbox deve ser removida, exibindo apenas uma única frase alinhada ao botão correspondente:
- Se o botão for **"Continuar"**, a frase deve começar com **"Ao continuar"**.
- Se o botão for **"Finalizar"**, a frase deve começar com **"Ao finalizar"**.
- A frase deve incluir **"você aceita"** + o nome do documento vinculado (termos e condições de uso, termos de criação de conta, etc.).

**Exemplos Corretos:**
- "Ao continuar, você aceita nossos termos e condições." – Botão: **Continuar**
- "Ao finalizar, você aceita nossos termos de uso." – Botão: **Finalizar pedido**
- "Ao assinar, você aceita nossas condições." – Botão: **Assinar Netflix**

**Exemplos Incorretos:**
- "Clique aqui para aceitar os termos e condições."
- "Ao prosseguir, você concorda com nossos termos."

**Observação:** Se houver falta de espaço ou criação de viúvas, é permitido remover "de uso" na frase.

**Exceções:**
- Novas variações só podem existir com pedido jurídico e aprovação de Content Ops.
- Em outros produtos, como **Meu Vivo Empresas**, o checkbox pode ser utilizado, mas deve seguir a mesma estrutura. 
- Caso o checkbox seja utilizado, a frase padrão é:
  ☑️ **Aceito os termos e condições de uso**

---

## Botões e Entrypoints
Para garantir ações visíveis e intuitivas, os botões e entrypoints devem ser:

- **Identificáveis:** Fáceis de encontrar e específicos.
- **Antecipados:** Devem indicar claramente a ação que será realizada.

### Regras para Construção de Botões e Entrypoints

1. **Modo verbal:** Use **verbos no infinitivo** (terminados em -ar, -er, -ir) para indicar a ação executada. O **uso do imperativo é proibido**, pois transmite tom impositivo.
2. **Apenas uma linha:** Botões não podem ultrapassar uma linha. Limite de **3 palavras** ou **até 20 caracteres**.
3. **Com contexto:** Devem conter **verbo + substantivo** para indicar a ação. Exemplo: "Ativar Netflix"
4. **Sem pontuação:** Não use pontuação, exceto se exigir o uso de vírgula.
5. **Sem artigos:** Evite "o, a, os, as, um, uma", pois aumentam a quantidade de caracteres sem necessidade.
6. **Apenas a primeira palavra em maiúscula:** Exceto quando houver nomes próprios, comerciais ou localidades.
7. **Linguagem simples:** Evite jargões técnicos e termos internos. O foco é a clareza.

### Botões Padronizados
Certas ações já possuem botões definidos para padronização:

- **"Entendi"**: Para telas de sucesso ou confirmação final.
- **"Ir para o início" / "Ir pro início"**: Em botões secundários que redirecionam para a home do app ou início do fluxo.

**Exemplos Corretos:**
- "Conhecer benefícios"
- "Ativar Forbes"
- "Ir pro início"

**Exemplos Incorretos:**
- "Conheça os benefícios"
- "Ative já o Forbes"
- "Voltar pro início"

**Exceções:**
- A única exceção ao **uso de verbos no infinitivo** ocorre quando um rótulo identifica uma seção sem direcionar diretamente para uma ação, como:
  - **"Suporte técnico"**, **"Serviços digitais"**, **"Vivo Travel"**.
- **Uso de maiúscula:** Quando houver nomes próprios, comerciais ou localidades, a regra pode ser flexibilizada. Exemplo:
  - **"Conhecer Vivo Fibra"** (em vez de "Conhecer vivo fibra").

**Explicação:**
- **Verbos no infinitivo**: O uso de infinitivo torna a ação mais clara e neutra, evitando a sensação de comando.
- **Acessibilidade**: Botões descritivos ajudam usuários de leitores de tela e pessoas neurodivergentes a entenderem a ação rapidamente.


---

## Empty States
Empty states são telas ou cards que aparecem quando não há conteúdo para exibir ou quando algo inesperado ocorre na jornada. Eles servem para explicar à pessoa usuária como alterar esse cenário.

### Regras para Construção de Empty States:
1. **Textos Educativos**: Explique o cenário atual e, quando possível, como mudá-lo.
2. **Textos Curtos e Diretos**: Use frases simples, em ordem direta (sujeito + verbo + complemento).
3. **Incentivo à Ação**: Use expressões como "Que tal?" ou "Confira nossa loja" para incentivar a pessoa a tomar uma atitude.
4. **Evite Interjeições e Humor**: Não use "Ops!" ou "Poxa", pois podem soar provocativos ou irritantes.


### Regras para Empty States em Telas:
- **Ícones**: Use o ícone de informação, exceto em casos de erro, onde o ícone de alerta é obrigatório.
- **Título**: Máximo de 2 linhas (cerca de 67 caracteres, sem viúvas).
- **Descrição**: Máximo de 2 linhas (cerca de 76 caracteres).
- **Botões**: Máximo de 25 caracteres, sempre com verbos no infinitivo.

### Regras para Empty States em Cards:
- **Título**: 1 linha (cerca de 30 caracteres) ou 2 linhas, se necessário.
- **Descrição**: Se o título tem uma linha, a descrição pode ter duas (até 65 caracteres). Caso contrário, apenas uma.
- **Botões**: Máximo de 25 caracteres, com verbos no infinitivo.

### Padrões de Uso:
Separamos algumas das frases-padrão a serem usadas nos títulos dos empty states, de acordo com o cenário de uso. É permitido fazer variações das descrições, desde que sejam levadas em conta as boas práticas de UX Writing e Acessibilidade.

1. **Cenário de Retorno de Ação da Pessoa Usuária**:
Quando a pessoa usuária tenta fazer algo, mas não temos um retorno. 
   - **Título**: "Nenhum/Nenhuma + contexto + foi encontrado".
   - **Descrição**: Dê instruções claras para refazer a ação.

   - **Exemplo Correto**:
     - Título: "Nenhum parceiro foi encontrado"
     - Descrição: "Você pode tentar buscar por outros parceiros"
     - Botão: "Refazer busca"
   - **Exemplo Incorreto**:
     - "Não encontramos nenhum protocolo"
     - "Não conseguimos encontrar esse parceiro"

2. **Cenário de Primeiro Uso**:
Quando a pessoa usuária ainda não assinou um serviço ou vai fazer algo pela primeira vez. 
   - **Título**: "Você ainda não + verbo no passado + contexto".
   - **Descrição**: Convide para ação com "Que tal + verbo + contexto?".

   - **Exemplo Correto**:
     - Título: "Você ainda não assinou um serviço digital"
     - Descrição: "Que tal conhecer algumas opções?"
     - Botão: "Conhecer serviços"

3. **Cenário de Ação Completa ou Limpa**:
Quando não há novas informações para exibir, naquele momento, para a pessoa usuária – seja porque ela já acessou tudo, seja porque o ciclo ainda não fechou. 
   - **Título**: "Nenhum/Nenhuma + contexto + por aqui".
   - **Descrição**: Antecipe alertas ou próximas etapas.

   - **Exemplo Correto**:
     - Título: "Nenhuma notificação por aqui"
     - Descrição: "A sua fatura ainda não fechou. A gente avisa quando isso acontecer."
     - Botão: "Ir pro início"

4. **Cenário de Erro**:
Quando temos uma situação de empty state gerada por um erro do nosso sistema.
   - **Título**: "Algo deu errado por aqui".
   - **Descrição**: Explique o erro e sugira uma solução.

   - **Exemplo Correto**:
     - Título: "Algo deu errado por aqui"
     - Descrição: "Não foi possível carregar o seu consumo. Você pode tentar de novo mais tarde."
     - Botão: "Ir pro início"

### Exceções:
- Em **Meu Vivo Empresas**, há o cenário em que a pessoa usuária pode não ter permissão para realizar determinada busca, então, nesse caso, o padrão de fraseologia é o mesmo, mas adicionamos essa informação ao fim da sentença.
   - **Exemplo Corretos**:
     - Nenhuma linha foi encontrada. Verifique se você tem permissão para acessar a área


---

## Mensagens de Erro e telas de erro
As mensagens de erro ou telas de erro devem reduzir a frustração das pessoas usuárias, informando de maneira clara o que aconteceu e como proceder.

### Regras para Construção de Mensagens de Erro
1. **Evite Mensagens Ambíguas**: Seja específico sobre o erro e evite mensagens genéricas e termos vagos como "Ocorreu um problema". Explique o que deu errado.

2. **Textos Curtos e Diretos**: Use frases curtas e diretas.
   - **Exemplo Correto**: "Tem algo errado com sua internet. Confira sua conexão e tente recarregar a página."
   - **Exemplo Incorreto**: "Se você está vendo essa tela, é porque pode ter algum problema com sua internet."

3. **Humanize as mensagens:** Erros são inesperados e frustrantes. Um tom empático pode melhorar a experiência.
   - **Exemplo Correto**: "Estamos melhorando as coisas por aqui. Você pode fazer isso de novo mais tarde."
   - **Exemplo Incorreto**: "Não foi possível realizar a operação. Tente novamente mais tarde."

4. **Minimize o Esforço da Pessoa Usuária**: Forneça soluções claras e práticas.
   - **Exemplo Correto**: "Não vai dar pra fazer seus resgates agora. Confira o regulamento da oferta, lá tem tudo bem explicado."
   - **Exemplo Incorreto**: "O resgate não pode ser realizado, clique em voltar e consulte o regulamento desta oferta."

5. **Formato de Informações**: Deixe claro como preencher formulários.
   - **Exemplo Correto**: "Sua senha deve ter uma letra maiúscula."
   - **Exemplo Incorreto**: "Sua senha deve corresponder a todos os requisitos mínimos."

6. **Evite Termos Capacitistas**: Não use termos como "Digite", "Veja" ou "Clique".
   - **Exemplo Correto**: "Preencha com um CPF válido."
   - **Exemplo Incorreto**: "Digite um CPF ou e-mail válido."

7. **Tentativas e Bloqueio**: Informe quantas tentativas restam e o que acontecerá em caso de bloqueio.
   - **Exemplo Correto**: "Algo deu errado ao validar o código. Você pode usar o código recebido mais 3 vezes."
   - **Exemplo Incorreto**: "Código inválido. Você tem mais 3 tentativas."

8. **Evite Humor**: Não use piadas, emojis ou interjeições.
   - **Exemplo Correto**: "Algo deu errado ao acessar o sistema."
   - **Exemplo Incorreto**: "Ops! Tem algo de errado por aqui, hein..."

### Arquitetura das Telas com mensagens de Erro 
As telas de erro apresentam um template, determinado pelo nosso Design System, e o uso é obrigatório.

#### Título
- Use, no máximo, **2 linhas** (cerca de 46 caracteres) para apresentar o título.
- Trabalhe a quebra da frase para que fique visualmente harmônica, evitando viúvas.
- **Não use interjeições** como "Ops!" e "Poxa!".

##### Tipos de Título:
1. **Erro Genérico**:  
   Use a construção: **"Algo deu errado com/ao + contexto da jornada"**.  
   - Exemplo: "Algo deu errado ao carregar sua fatura."

2. **Erro Conhecido**:  
   Use a voz passiva: **"A/O/Seu/Sua + contexto + não foi + verbo no passado"**.  
   - Exemplo: "Sua solicitação não foi processada."

##### Descrição
- Use, no máximo, **2 linhas ou um parágrafo** (cerca de 105 caracteres) para complementar a mensagem de erro.
- Trabalhe a quebra da frase para evitar viúvas e garantir harmonia visual.
- O texto deve:
  - Complementar as informações do título.
  - Contextualizar e explicar o motivo do erro, quando possível.
  - Apresentar como a pessoa usuária pode prosseguir na navegação (solução ou contorno do problema).

##### Botões em mensagens de erro
- Use **verbos comuns ao fluxo ou serviço**.
- Se a ação do botão estiver descrita no texto, **repita o mesmo verbo** (não use sinônimos).
- Consulte a seção **Botões e Entrypoints** para mais detalhes sobre a construção de botões.

### Padrões de Conteúdo em Telas de Erro:
1. **Erro em Serviço**:
   - **Título**: "Algo deu errado com este serviço."
   - **Descrição**: "Você pode tentar de novo agora ou fazer isso mais tarde."
   - **Botão**: "Tentar de novo / Ir para o início"

2. **Erro por Manutenção**:
   - **Título**: "Estamos melhorando as coisas por aqui."
   - **Descrição**: "Você pode tentar fazer isso de novo mais tarde."
   - **Botão**: "Ir para o início"

3. **Erro Genérico**:
   - **Título**: "Algo deu errado por aqui."
   - **Descrição**: "Você pode tentar de novo agora ou fazer isso mais tarde."
   - **Botão**: "Tentar de novo / Ir para o início"

4. **Erros Específicos - Cenário Web**:
   - **Erro 500**:
     - Título: "Algo deu errado com este serviço."
     - Descrição: "Ele não está funcionando agora, mas você pode tentar fazer isso de novo mais tarde."
     - Botão: "Ir para o início"
   - **Erro 400**:
     - Título: "Algo deu errado por aqui."
     - Descrição: "A página que você procura não existe."
     - Botão: "Ir para o início"

### Padrões de Fraseologias em Formulários
Separamos algumas frases-padrão a serem usadas, de acordo com o erro que precisamos exibir para a pessoa usuária. Lembre-se de que essas frases-padrão servem apenas como erro dentro dos formulários e não devem ser aplicadas a títulos ou textos nas telas.

#### Empty State
- **Exemplos Corretos**:
  - "Você precisa preencher este campo com um código pra continuar."
  - "Você precisa informar um CPF pra continuar."
- **Exemplos Incorretos**:
  - "Preencha o campo código."
  - "Preencha com um CPF."

#### Confirmar uma Informação
- **Exemplos Corretos**:
  - "É preciso preencher este campo com uma senha pra continuar."
  - "Você tem que confirmar a sua senha pra continuar."
  - "Os e-mails devem ser iguais."
  - "As senhas devem ser iguais."
- **Exemplos Incorretos**:
  - "Preencha o campo senha."
  - "Confirme a senha."
  - "Os e-mails devem ser idênticos."
  - "As senhas devem ser idênticas."

#### Mensagens de Erro de Preenchimento
- **Exemplos Corretos**:
  - "Tem algo errado com o CPF que você informou. Dá/Dê uma conferida."
  - "Tem algo errado com o código que você informou. Dá/Dê uma conferida."
  - "As informações não estão corretas. Você tem mais 2 tentativas."
  - "As informações não estão corretas. Última tentativa antes do bloqueio."
  - "Bloqueamos seu acesso. Você pode criar uma senha em 24 horas."
  - "Sua senha expirou, mas você pode criar uma nova [Criar nova senha]."
- **Exemplos Incorretos**:
  - "CPF inválido."
  - "Código inválido."
  - "O que você informou não bate com a sua senha. Você tem mais 2 tentativas."
  - "O que você informou não bate com a sua senha. Na próxima tentativa incorreta seu acesso será bloqueado."
  - "Bloqueamos o seu acesso. Volte em 24h e crie uma nova senha."
  - "Sua senha expirou. Entre em 'Esqueci minha senha' para criar uma nova."

#### Mensagens de erro quando o Input ou informação Está Fora do Padrão/Formato
- **Exemplos Corretos**:
  - "Sua senha não está no formato que a gente precisa. Dá/Dê uma conferida."
  - "Informe um número de celular com o formato do tipo: (00) 00000-0000."
  - "Informe um e-mail válido com o formato do tipo: joao@gmail.com."
- **Exemplos Incorretos**:
  - "Senha deve corresponder a todos os requisitos mínimos."

#### Mensagens Quando a Pessoa Usuária Erra em Formulário que Oferece Várias Tentativas
- **Exemplos Corretos**:
  - "Algo deu errado ao validar. Você pode usar o código recebido mais 4/3/2 vezes."
  - "Algo deu errado ao validar. Essa é a última tentativa. Caso erre, você volta pro início da atualização cadastral."
  - "Algo deu errado ao validar. Dá/Dê uma conferida."
  - "Algo deu errado ao validar. Na próxima tentativa incorreta, seu acesso será bloqueado."
  - "Seu acesso foi bloqueado. Tente novamente em 24 horas."
- **Exemplos Incorretos**:
  - "Código inválido. Você tem mais 4/3/2 tentativas."
  - "Código inválido. Você pode fazer mais uma tentativa. Em caso de erro, você vai ser redirecionado."
  - "Tem algo errado com este código. Na próxima tentativa incorreta seu acesso será bloqueado."
  - "Bloquearemos seu acesso. Você pode tentar de novo em 24 horas."

#### Exceções
- **Aplicações em B2B**: Por causa do tamanho das fontes e das telas em B2B, permitimos o uso de frases mais curtas no helper texts em formulários. Usamos 31 caracteres sem espaço ou 35 com espaço. Com a diminuição das frases, optamos por:
  - "Tem algo errado, dê uma conferida."
  - "Você precisa preencher este campo."

---

## Filtros de Períodos de Tempo ou Datepickers
Os filtros de períodos são usados para buscar informações retroativas sobre assinaturas, pedidos, extratos, saldos e atendimentos na Vivo. Como estão em telas com conteúdo denso, devem ser concisos, claros e objetivos para não aumentar a carga cognitiva. Além disso, o texto precisa indicar exatamente os dias, meses ou anos disponíveis para pesquisa, evitando cálculos ou associações.

### Regras para Criação de Períodos de Tempo e Datepickers

#### Use o padrão: Algarismo + Dias
Para escrever um filtro, use apenas o algarismo que representa o período permitido na jornada ou contexto, seguido da palavra "dia" ou "dias". Não utilize adjetivos como “últimos” ou “primeiros”.

**Exemplos Corretos:**
- 7 dias
- 15 dias
- 30 dias
- 45 dias

**Exemplos Incorretos:**
- Última semana
- Últimos 15 dias
- Primeiros 10 dias
- Último mês
- Um mês e meio

#### Priorize Dias
O período disponível varia por funcionalidade, mas recomendamos priorizar 7 dias (semanal), 15 dias (quinzenal) e 30 dias (mensal). Evite expressões como “na última semana” e “último mês”, pois podem causar dúvidas. Prefira “7 dias” e “30 dias” para mais clareza.

#### Sem Pontuação
Nenhum dos nossos filtros recebe pontuação ao final da frase.

**Exemplos Corretos:**
- 2 meses
- 7 dias

**Exemplos Incorretos:**
- 2 meses.
- 7 dias.

#### Exceções: Fluxos com Grande Quantidade de Informação
Em jornadas com períodos históricos extensos, podemos utilizar meses e até anos. Se nos referimos a um período completo e contínuo maior que 30 dias, usamos meses. Acima de 12 meses, utilizamos anos.

**Exemplos Corretos:**
- 2 meses
- 3 meses
- 12 meses
- 2022
- 2023
- 2024

**Exemplos Incorretos:**
- Últimos 60 dias
- Últimos 3 meses
- 270 dias
- Último ano
- Últimos 2 anos

---

## FAQ
A FAQ reúne as perguntas mais frequentes das pessoas usuárias e suas respostas. No app Vivo, recebe o nome de **Principais Dúvidas**.
Seu principal objetivo é oferecer um autoatendimento rápido, simples e conciso.

### Regras para Construção de FAQs

#### Construa um Texto Simples e Objetivo
Priorize frases curtas e diretas, trazendo apenas uma informação por frase para facilitar a leitura e compreensão.

#### Responda uma Dúvida por Vez
Divida dúvidas extensas em múltiplas perguntas para evitar sobrecarga de informações e garantir entendimento.

#### Priorize as Dúvidas
Antes de produzir uma FAQ, consulte as áreas mais próximas aos clientes para identificar as perguntas mais relevantes. Defina uma ordem de prioridade para facilitar a organização dentro do app.

#### Zele pelo Bom Português
Evite erros gramaticais e garanta clareza. Leia o texto em voz alta, utilize um leitor de tela ou peça feedback para garantir compreensão.

#### Cuidado com o Uso de Caixa Alta
Utilize letras maiúsculas apenas no início de frases, em nomes próprios ou após pontuação.

#### Priorize o Uso de Verbos no Infinitivo
Para tornar a comunicação menos impositiva, utilize verbos no infinitivo sempre que possível.

**Exemplo Correto:**
- "Abrir o aplicativo."

**Exemplo Incorreto:**
- "Abra o aplicativo."

#### Não Use Termos Internos
Evite jargões e nomenclaturas desconhecidas pelo público. Pergunte-se: "Se fosse uma pessoa com pouca familiaridade, ela entenderia?" Se a resposta for "não", refaça o texto.

#### Mantenha o Tom Conversacional
A comunicação no app Vivo deve ser afetiva, transparente e acessível.

#### Não Use Emojis ou Emoticons
Por acessibilidade, evite emoticons como ";)", pois leitores de tela podem interpretá-los de forma errada. Emojis também devem ser evitados para reduzir a carga informacional na tela.

#### Descreva Itens em Lista Numerada
Para passo a passo, utilize listas numeradas. O ideal é limitar a três passos para evitar esforço cognitivo excessivo. Para outros tópicos, utilize bullet points.

#### Coloque Links Apenas ao Final do Texto
Links devem ser inseridos ao final do texto, pois links no meio não podem ser tagueados corretamente.

### Padrões de Conteúdo para Construção de FAQs

1. **Pergunta**
   - Sempre em formato de pergunta, com ponto de interrogação ao final. Lembre-se que a pergunta serve como entrypoint.

2. **Title**
   - Repetição da pergunta da FAQ. No CMS, deve ter marcação **H1 (heading 1)** para acessibilidade.

3. **Markdown Section**
   - Responda a pergunta de forma simples e completa.
   - Use listas numeradas apenas quando necessário.
   - Evite itálico e sublinhado. Use negrito com cuidado para destacar palavras relevantes ou números de telefone.
   - Caso precise criar um subtítulo, use **H2 (heading 2)**.
   - Insira links internos apenas ao final do texto.

---

## Headers
O header, headers ou cabeçalho é o principal espaço de relacionamento, informação e comunicação do **App Vivo** com o cliente. Como é a primeira informação que a pessoa usuária recebe ao acessar o app, criamos mensagens exclusivas, inteligentes e específicas para cada caso de uso.

### Regras para Criação de Headers e Cabeçalhos
- **75 caracteres:** Essa quantidade de caracteres é obrigatória para headers em *Pra você*, garantindo concisão e boa experiência de leitura.
- **Texto em até 3 linhas:** Seguindo a regra dos 75 caracteres, o texto deve ser limitado a 3 linhas, evitando palavras isoladas (viúvas).
- **Uso de botões:** O botão deve seguir a estrutura definida na seção de botões e entrypoints, sempre alinhado ao verbo, produto ou serviço mencionado no texto.
- **Pontuação:** Headers não devem conter ponto final. São permitidos *interrogação (?)*, *exclamação (!)*, *dois pontos (:)* e *vírgulas (,)* quando necessário.
- **Termos capacitistas:** Evite termos excludentes como “Dá uma olhada” ou “Dedos cruzados”. Consulte a seção de **Boas Práticas de Acessibilidade** se houver dúvidas.

**Exemplos Corretos:**
- "Que tal conferir os benefícios que a Vivo tem para o seu plano?"
- "Hoje é dia do sorteio da nossa promoção! Estamos torcendo pra você ganhar."

**Exemplos Incorretos:**
- "Corre aqui pra conferir os benefícios que a Vivo tem para o seu plano!"
- "Hoje é dia do sorteio da nossa promoção! Dedos cruzados pra você ganhar."

---

## In-Apps
In-apps são mensagens exibidas na tela, em diferentes formatos, usadas para informar as pessoas usuárias sobre novidades no aplicativo ou serviço. O uso é opcional e depende do nível de familiaridade entre a pessoa usuária e a interface.

### Critérios para Uso de In-Apps
Antes de usar um in-app, avalie:
- Se o serviço tem navegação ou funções não convencionais.
- Se a funcionalidade é nova.
- Se há mudanças significativas no serviço.

### Tipos de In-Apps

#### **Onboarding**
- Exibido quando a pessoa usuária acessa o app pela primeira vez.
- Abre em *modal* e pode estar em formato *carrossel*.
- **Uso:** Informações essenciais do app, mudanças significativas ou passo a passo de funcionalidades complexas.
- **Não use para:** Promoções ou novidades explicáveis em uma única tela.

#### **Localizado**
- Aparece quando a pessoa usuária clica em uma área específica do app (ex.: *Mais, Meu Plano*).
- Abre em *modal* e pode ser usada apenas em uma tela ou em formato *carrossel*.
- **Uso:** Informações gerais e relevantes sobre produtos ou serviços.
- **Não use para:** Promoções.

#### **Contextual**
- Aparece dentro de um contexto específico onde a informação faça sentido e em formato de card.
- **Uso:** Mensagens não urgentes, como promoções e ofertas.
- **Não use para:** Informações críticas que impactam a experiência do app.

#### **Linkado**
- Exibido em tela cheia, complementando notificações push ou outros in-apps. Abre em *modal* e é composto por uma única tela
- **Uso:** Instruções detalhadas, como ativação de promoções divulgadas em push.
- **Não use de forma independente.**

### Regras para Criação de In-Apps
- **Evite muitas telas:** A informação deve ser rápida e direta. Mostre apenas os benefícios mais relevantes.
- **Um tópico por vez:** Cada tela, slide ou etapa deve abordar um único item.
- **Mantenha a consistência:** Use sempre os mesmos termos da interface.
**Exemplo**: Se a interface diz "Baixar o arquivo", não use "Fazer download" no botão.
- **Não explique o óbvio:** Funções convencionais, como o botão "voltar", não precisam ser explicadas. Caso tal informação seja necessária, adicione mais detalhes que não estão evidentes, como: numa página de resultado de busca, pode ser dito “Você pode refazer sua busca sempre que precisar”.
- **Cuidado com imagens:** Use exemplos de tela para apontar novidades ou serviços. Ilustrações devem complementar o texto.
- **Facilite o onboarding:** A navegação deve ser clara para iniciar o uso do app.

### **Padrões – App Vivo In-App**
Para o **App Vivo**, devido às limitações do **CMS** que hospeda os in-apps, seguimos especificações rigorosas para garantir consistência e acessibilidade. A documentação completa pode ser consultada no **Novum GitBook**: [Novum GitBook](https://tef-novum.gitbook.io/in-app-message/-LtzGpuJbnsqRTGT-kYV/).

#### **In-apps Modal**

**Regras Gerais:**
- O botão de fechar (**X**) é opcional.
- **Imagem com alt text, título, texto (parágrafo ou checklist) e ao menos um botão são obrigatórios**.
- Quando há **carrossel**, todas as telas (exceto a última) devem manter a mesma estrutura: 
  - Podem não ter botões ou 
  - Devem conter o botão **“Próximo”**.
- O **título** deve ter, no máximo, **56 caracteres**.
- O **texto em parágrafo** deve ter, no máximo, **140 caracteres**.
- Se houver **apenas uma tela**, o texto pode ser um **checklist** (até três itens, sendo o primeiro obrigatório e os outros dois opcionais). Cada item pode ter até **28 caracteres**.
- A **imagem** deve ter um **texto alternativo** de, no máximo, **56 caracteres**, garantindo acessibilidade caso não carregue.

**Exemplo Correto:**
- **Título:** Mais segurança para você
- **Descrição:** Quer ter mais proteção no acesso? Em Segurança e privacidade, você encontra funcionalidades que ajudam a ter mais confiança ao usar o app.
- **Botão:** Acessar agora

#### **In-apps Card**

**Regras Gerais:**
- O botão de fechar (**X**) é opcional.
- **Título, texto de descrição e imagem com alt text são obrigatórios**.
- O **título** deve ter, no máximo, **26 caracteres**.
- O **texto de descrição** deve ter, no máximo, **68 caracteres**.
- A **imagem** deve ter um **texto alternativo** de, no máximo, **56 caracteres**.

**Exemplo Correto:**
- **Título:** Loja Vivo
- **Descrição:** Ganhe até R$ 900 na compra do seu novo Galaxy

---

## Páginas Internas
Páginas internas são mais explicativas e trazem informações completas sobre promoções, produtos ou serviços. As solicitações de criação e publicação devem ser enviadas ao time de Produtos.

### Tipos de Páginas Internas
- **Informativas:** Comunicam benefícios ou lançamentos (ex.: Revista Velvet).
- **Promocionais/Perenes:** Promoções permanentes (ex.: Vivo Valoriza).
- **Promocionais/Limitadas:** Ações de curta duração (ex.: Semana do Bem-Estar).
- **Relacionamento:** Fortalecem a relação com o cliente (ex.: Vídeo da Copa).

### Regras para Criação de Páginas Internas
- **Título em até 3 linhas:** Deve destacar o principal benefício e evitar ponto final.
- **Texto secundário em até 3 linhas:** Complementa o título com informações adicionais.
- **Uso de botões:** Seguir as regras de botões e entrypoints, evitando termos como "Ver mais" e "Clique aqui".
- **Botões secundários:** Permitidos para ações complementares, seguindo os mesmos padrões.
- **Acessibilidade:** Não insira texto em imagens e utilize texto alternativo. Existe um campo próprio para isso no CMS.

### Cenários de Uso de páginas internas
- **Vantagens:** O que torna o produto/serviço único? Destaque os diferenciais do produto ou serviço.
- **Comparações:** Como seu produto se diferencia da concorrência? Mostre como o produto ou serviço se diferencia da concorrência.
- **Passo a Passo:** O que a pessoa usuária deve fazer? Explique como obter o benefício.
- **Lista de Dúvidas:** Há informações técnicas essenciais? Responda a dúvidas comuns sobre o produto ou serviço.

---

## Status Tags
Status tags são marcadores visuais e textuais que indicam a etapa de um processo. Elas devem ser padronizadas para evitar aumentar a carga cognitiva da pessoa usuária.

### Tipos de Status Tags

#### **Tags de Sucesso**
Indicam conclusão de um processo sem problemas. Usam a cor verde.
- **Exemplos:** Disponível, Concluído.

#### **Tags de Alerta**
Exigem atenção da pessoa usuária. Usam a cor laranja.
- **Exemplos:** Pronto para pagar, Em andamento.

#### **Tags de Falha/Erro**
Indicam problemas no processo. Usam a cor vermelha.
- **Exemplos:** Atrasado, Bloqueado, Cancelado.

#### **Tags de Exceção**
Usadas para status específicos que não se enquadram nas categorias anteriores, como inatividade ou expiração.
- **Exemplos:** Aguardando sua resposta, Nova, Expirada.

### Regras para Construção de Status Tags
- **Informe o time de Content Design Ops** ao criar novas tags.
- **consulte tags existentes** antes de criar novas.
- **Limite de 24 caracteres com espaços.**
- **Pode conter ícones, desde que não comprometam a interface.**

---

## Telas de Informação e mensagens de informação ou feedback
As telas de informação ou feedback explicam cenários e situações que precisam da atenção da pessoa usuária. Elas podem ser frustrantes por causarem um passo a mais na jornada, por isso, optamos por textos simples, diretos e informativos.

### Regras para Criação de Telas de Informação
- **Seja específico:** Evite mensagens ambíguas. Seja direto e objetivo. Mensagens genéricas podem gerar dúvidas.
- **Vá direto ao ponto:** Prefira textos curtos e em ordem direta (*sujeito + verbo + complemento*).
- **Facilite a ação da pessoa usuária:** Oriente sobre os próximos passos de forma objetiva.
- **Evite humor:** Mensagens devem ser respeitosas e informativas, sem piadas ou emojis.

**Exemplos Corretos:**
- *Bloqueio temporário. Por segurança, seu acesso foi bloqueado por 4 horas. Você pode tentar de novo após esse prazo.*

**Exemplos Incorretos:**
- *Se você está vendo essa tela, é porque seu acesso pode estar bloqueado. Tente novamente.*

### Estrutura das Telas de Informação
1. **Título:**
   - Até 2 linhas.
   - Evite viúvas (palavra solitária na última linha).
2. **Descrição:**
   - Até 3 linhas, complementando o título e orientando a ação.
   - Não use ponto final em descrições.
3. **Botões:**
   - Utilize verbos alinhados ao fluxo e evite sinônimos desnecessários.
   - Consulte a seção de *Botões e EntryPoints* antes de criar.

### Cenários de Uso de telas de informação
**1. Tela de Informação Durante a Jornada**
As telas de informações, como o próprio nome já diz, aparecem em uma jornada pra trazer alguma informação que seja relevante no fluxo seguido. Elas trazem explicações e orientações sobre os próximos passos pra conclusão da jornada iniciada 
**Exemplo:**
- **Título:** Sua assinatura ainda não foi ativada
- **Descrição:** Caso tenha ativado a assinatura, em alguns instantes, ela estará pronta pra você aproveitar.
- **Botão Principal:** Continuar ativação
- **Botão Secundário:** Entendi

**2. Tela de Informação em Sucesso Parcial**
Se a pessoa usuária entrou em uma jornada, mas o sucesso não foi completo e ainda precisa ainda de outra etapa a ser realizada, definimos que não usaremos a tela de sucesso em púrpura. Nesse caso, também usamos o Info Feedback.
**Exemplo**
- **Título:** Você bloqueou uma linha
- **Descrição:** Algo deu errado ao bloquear outras linhas. Tente de novo mais tarde.
- **Botão:** Ir para o início

---

## Telas de Loading ou telas de carregamento
As telas de loading, telas de carregamento ou mensagens de carregamento comunicam o status de solicitações para diminuir frustrações em caso de espera. Elas aparecem quando a pessoa usuária precisa esperar alguma ação da Vivo, como uma consulta ou confirmação de dados, diminuindo frustrações em tempos de espera.

### Regras para Criação de Telas de Loading
- **Uso do verbo no gerúndio:** Mantém a ideia de ação em andamento (*alterando, processando, confirmando*).
- **Consistência:** O verbo deve estar alinhado ao fluxo principal.
- **Texto conciso:** Máximo de 30 caracteres e 1 linha.
- **Sem pontuação:** Não utilizamos ponto final ou vírgulas.
- **Maiúsculas apenas na primeira palavra:** Exceto em nomes próprios ou comerciais.
- **Uso de números:** Algarismos são permitidos para indicar quantidade.
- **Linguagem simples:** Sem jargões técnicos ou termos internos.

**Exemplos Corretos:**
- *Alterando seu endereço*
- *Confirmando as informações*
- *Processando seu pedido*

**Exemplos Incorretos:**
- *Vamos alterar seu endereço*
- *Informações sendo confirmadas*
- *Seu pedido está sendo processado*

### Exceção: Textos Secundários
Se o tempo de espera for maior que o esperado, uma segunda linha pode ser adicionada. **Exemplo:** - *Por favor, aguarde*, - *Aguarde mais um pouco*

---

## Telas de Sucesso e mensagens de sucesso
As telas de sucesso ou mensagens de sucesso afirmam explicitamente o sucesso de um processo e fornecem informações extras ou ações a serem realizadas em seguida. Elas são usadas em jornadas longas ou processos de compras devem trazer, no máximo, duas ações para orientar as pessoas usuárias para o que for melhor a seguir.
Por padrão, tente comunicar o sucesso de uma ação ou processo implicitamente na interface da pessoa usuária sem usar um componente específico. Idealmente, o resultado dessa ação ou fluxo deve ser claramente visível na própria interface.

### Regras para Criação de Telas de Sucesso
- **Título de até 2 linhas:** Evitar viúvas.
- **Não usamos emojis.**
- **Estrutura do título:**
  1. **Identificação da pessoa usuária** (*Você*).
  2. **Feedback da ação realizada** (*alterou, cadastrou, enviou*).
  3. **Complemento primário** (*Produto ou serviço relacionado.*).
  4. **Complemento secundário** (*se houver informação extra relevante*).

- **Voz passiva:** Permitida em títulos muito longos ou com destaque para produtos.

**Exemplo Correto:**
- *Você alterou seu endereço.*

**Corpo do Texto:**
- Máximo de **3 blocos** com até **3 linhas cada**.
- Informações organizadas conforme a relevância.
- Períodos de tempo seguem as diretrizes da seção específica.

**Botões:**
- Seguem as regras de *Botões e EntryPoints*.
- O botão de retorno para home já é padronizado: *Ir para o início*.

### Casos de Sucesso Parcial
- Use telas de informação em vez de telas de sucesso quando o processo não foi completamente concluído.
- **Exemplo**:
  - Título: "Você bloqueou uma linha."
  - Descrição: "Algo deu errado ao bloquear outras linhas. Tente de novo mais tarde."
  - Botão: "Ir para o início"

---

## Títulos em Interfaces
Os títulos são usados para trazer feedbacks, reportar erros, comunicar próximos passos ou dar nome às seções. Eles devem ser sucintos e claros.Os títulos informam em que momento da jornada a pessoa usuária está e qual ação ela realizou ou deve realizar.

### Regras para Criação de Títulos em Interfaces
- **Até 2 linhas:** Para melhor legibilidade. O título deve informar o que há de mais relevante.
- **Sem interjeições:** Nada de *Ops!* ou *Poxa!*, para evitar frustrações.
- **Sem ponto final, exceto em frases duplas.**
- **Permitidos:** *Interrogação (?), exclamação (!), dois pontos (:), vírgula (,).*
- **Consultar diretrizes de telas de erro** e **Consultar diretrizes de telas de sucesso** para verificar se a mensagem se enquadra nesse cenário.
- **Caixa alta:** Apenas a primeira palavra deve ter letra maiúscula.
- **Exceção:** Nomes próprios, rótulos de seção e serviços Vivo.


---

## Mensagens sobre o Uso de Cookies
Mensagens sobre cookies devem ser claras, precisas e seguir as regras da **LGPD**.

### Regras para Construção de Textos sobre Cookies
Com o apoio do time **DPO** (Data Protection Officer, responsável pela aplicação e gestão legal de informações sobre dados), criamos uma lista de boas práticas e recomendações que devem ser seguidas na construção de mensagens sobre cookies.

#### Validação Jurídica
- O texto deve ser proposto pelos times responsáveis e validado pelo time jurídico e pelo DPO. **Não faça alterações sem consultar o time de Content Ops**.
- Em caso de dúvidas ou necessidade de ajustes, consulte o time de Content Ops antes de propor qualquer mudança.

#### Informações Claras e Específicas
- **Garanta que a pessoa usuária saiba o motivo do uso de cookies**:
  - Para estar em conformidade com a **LGPD**, o texto deve especificar a finalidade dos cookies de forma clara e objetiva.
  - Evite motivos genéricos. Explique exatamente para que os cookies serão usados.
  - **Exemplo Correto**:
    - Mensagem: "A Vivo utiliza cookies de sessão para melhorar sua experiência no site e apresentar ofertas personalizadas para você. Ao aceitá-los, você também concorda com a nossa política de privacidade."
    - Botões: "Aceitar todos os cookies", "Rejeitar todos os cookies", "Gerenciar cookies".
  - **Exemplo Incorreto**:
    - Mensagem: "A Vivo detém cookies para compartilhamento com empresas parceiras. Ao continuar navegando, você concorda com nossas políticas de dados."
    - Botões: "Concordar e fechar".

#### Acessibilidade e Clareza
- **As informações devem ser claras, precisas e facilmente acessíveis**:
  - A pessoa usuária precisa entender:
    - Qual tratamento a Vivo dará aos seus dados.
    - O período de retenção dos dados.
    - As finalidades específicas que justificam a coleta.
  - Informe que a pessoa usuária pode entrar em contato com os canais da Vivo para exercer seus direitos previstos na LGPD.

#### Opções de Gerenciamento de Cookies
- **Ofereça opções claras para aceitar, recusar ou gerenciar cookies**:
  - A LGPD garante que a pessoa usuária deve ter o direito de escolha. Rejeitar cookies deve ser tão simples quanto aceitá-los.
  - **Exemplos Corretos**:
    - Botões: "Aceitar cookies", "Recusar cookies", "Gerenciar cookies".
  - **Exemplos Incorretos**:
    - Botões: "Aceitar todos os cookies", "Concordar e fechar", "Concordar".

#### Tamanho do Texto
- **Mantenha o texto conciso e acessível**:
  - Embora as mensagens de cookies sejam obrigatórias, elas devem refletir o tom e voz da Vivo.
  - Evite textos longos e jargões técnicos ou jurídicos.
  - O objetivo é que a pessoa usuária leia a informação e decida como agir, sem se sentir sobrecarregada.

#### Envolvimento dos Times Jurídicos e Técnicos
- **Nenhuma alteração deve ser feita sem aprovação**:
  - Qualquer mudança no texto de cookies, por menor que seja, deve ser aprovada pelos times jurídicos e de Content Ops.
  - Em caso de dúvidas, consulte essas equipes antes de propor ajustes.

-->
