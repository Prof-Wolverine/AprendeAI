# 🎢 Aprende AI — Parque do Conhecimento

> **Quiz gamificado de Matemática para o Ensino Fundamental II**
> Aprender brincando, com avatar, mascotes, moedas e uma montanha do conhecimento.

![Status](https://img.shields.io/badge/status-ativo-brightgreen)
![Versão](https://img.shields.io/badge/versão-6.0-blue)
![Licença](https://img.shields.io/badge/licença-educacional-orange)
![HTML](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![CSS](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)

---

## 📖 Sobre o projeto

O **Aprende AI** é uma plataforma educacional gamificada, feita em **HTML/CSS/JavaScript puro** (sem frameworks, sem backend obrigatório), voltada para o **Ensino Fundamental II**.

O jogo transforma o estudo de matemática em uma experiência de parque de diversões: os alunos criam avatares, colecionam mascotes, ganham moedas e escalam a **Montanha do Conhecimento** com a turma.

### 🎯 Objetivo pedagógico

- Tornar o estudo de matemática **mais leve e motivador**
- Oferecer **feedback imediato** ao aluno
- Permitir que o professor **acompanhe o desempenho** da turma em tempo real
- Trabalhar **autonomia**, **persistência** e **metacognição** (o aluno pode refazer e melhorar)

---

## ✨ Funcionalidades

### 👩‍🎓 Para o estudante

- 🎨 **Avatar personalizável** (pele, cabelo, roupas, chapéus, asas, auras, cenários)
- 🐾 **24 mascotes** (sapo, capivara, tigre, dragão, fênix...)
- 🪙 **Economia de moedas** com loja rotativa semanal
- 🏅 **XP, níveis e desbloqueio progressivo** de mascotes
- ⛰️ **Montanha do Conhecimento** com ranking da turma
- ⚔️ **Duelo 1v1** contra colegas
- 🎯 **Desafio diário** com bônus
- 🎵 **Música ambiente** e efeitos sonoros
- 🌐 **Multilíngue** (PT / EN / ES)

### 👨‍🏫 Para o professor

- 🔑 **Painel do professor** (acesso com senha)
- ➕ **Cadastro de questões extras** por matéria
- 📊 **Dashboard** com gráficos de desempenho por matéria e turma
- ☁️ **Integração com Google Sheets** (ranking global)
- 📧 **Envio automático de resultados** por e-mail (FormSubmit)
- 📥 **Exportação de CSV** com todos os resultados

---

## 📚 Conteúdo curricular (24 matérias)

| Área | Matérias |
|---|---|
| **Números e Operações** | Operações com Naturais · Divisibilidade, MMC e MDC · Frações · Números Decimais · Porcentagem · Números Inteiros · Potenciação e Radiciação · Razão e Proporção |
| **Álgebra** | Expressões Algébricas · Equações do 1º Grau · Sistemas de Equações · Produtos Notáveis · Equações do 2º Grau · Funções |
| **Geometria** | Figuras Planas · Ângulos e Retas · Áreas e Perímetros · Geometria Espacial · Teorema de Pitágoras |
| **Grandezas e Medidas** | Unidades de Medida · Volume e Capacidade |
| **Estatística e Probabilidade** | Gráficos e Tabelas · Média, Moda e Mediana · Probabilidade |

> **500 questões geradas automaticamente por matéria**, em níveis fácil e médio, com embaralhamento das alternativas a cada rodada.

---

## 🚀 Como usar

### Para alunos

1. Acesse o link publicado: `https://SEU-USUARIO.github.io/aprende-ai/`
2. Cadastre-se com **nome completo**, **e-mail @escola** e **turma**
3. Escolha um assunto na barra lateral
4. Responda as questões
5. Clique em **"📧 Enviar Resultado ao Professor"** ao finalizar

### Para o professor

1. Acesse o jogo com qualquer conta
2. Na barra lateral, clique em **"🔑 Modo Professor"**
3. Senha padrão: `prof123` *(altere no código!)*
4. Cadastre questões extras ou configure integrações

---

## ⚙️ Configuração e personalização

Todas as configurações principais estão no objeto `CONFIG`, no início do `<script>` do arquivo `index.html`:

```javascript
const CONFIG = {
  teacherEmail: "ydvir.souza@escola.pr.gov.br",   // e-mail que recebe os resultados
  teacherPassword: "prof123",                      // senha do modo professor
  practiceMode: { questions: 10, timeSeconds: 0 },
  examMode: { questions: 20, timeSeconds: 20 * 60 },
  dailyMode: { questions: 5, timeSeconds: 0, bonusCoins: 100, bonusXP: 50 },
  duelMode: { questions: 5, timeSeconds: 0, winCoins: 80, winXP: 40 },
  questionsPerBank: 500,
  coinsPerCorrect: 20,
  examCoinMultiplier: 1.5,
  perfectBonus: 100,
  startingCoins: 100,
  xpPerCorrect: 10,
  examXpMultiplier: 1.5,
  perfectXpBonus: 50,
  formSubmitEndpoint: "https://formsubmit.co/ajax/ydvir.souza@escola.pr.gov.br"
};
