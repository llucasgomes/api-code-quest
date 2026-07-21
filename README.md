# CodeQueste — Documentação de Regras de Negócio

> Plataforma de perguntas de entrevista técnica (múltipla escolha) com progressão em RPG, inspirada na vibe de *Lineage II: Interlude* (XP, níveis, grades de equipamento, trilhas e PvP).

---

## 1. Visão Geral

O usuário cria um personagem e evolui puramente por **nível/XP**, subindo por **Grades** (Newbie → D → C → B → A → S), no mesmo espírito dos grades de itens do L2. Diferente da v1 deste documento, **não existe mais árvore de raça/classe fixa** — existe uma **Trilha** escolhida no Grade D, que se aprofunda em uma **Especialização** escolhida no Grade C, e volta a ficar transversal nos grades B, A e S.

Dois eixos independentes:
- **Grade** = dificuldade e estrutura de progressão (igual pra todo mundo).
- **Trilha / Especialização** = o tema das perguntas dentro de cada grade (escolhido pelo usuário).

---

## 2. Estrutura de Grades

| Grade | Nível | Trilha ativa? | O que acontece |
|---|---|---|---|
| **Newbie** | 1–19 | Nenhuma | Conteúdo 100% universal — fundamentos de programação |
| **D** | 20–39 | Escolhe a **Trilha** | Fundamentos da trilha escolhida, ainda sem especialização |
| **C** | 40–51 | Escolhe a **Especialização** | Aprofunda dentro da trilha, em um framework/stack/foco específico |
| **B** | 52–60 | Trilha "pausada" | Conteúdo transversal (ferramentas que todo pleno usa) |
| **A** | 61–71 | Volta à Especialização | Nível pleno, aprofundando a especialização escolhida no C |
| **S** | 72+ | Cross-domain | Nível sênior/arquiteto, mistura trilhas |

### 2.1 Regras de transição entre grades
- Subir de grade exige **nível mínimo** + **Quest de Grade**: uma prova com taxa mínima de acerto (ex: 80%), cronometrada.
- Reprovar a Quest de Grade não tira XP, mas aplica **cooldown de 24h** para nova tentativa.
- A escolha de Trilha (Grade D) e Especialização (Grade C) é **permanente** por padrão — só pode ser trocada com o item "Poção do Esquecimento" (1 uso, ver seção 6).
- Não existe downgrade de grade por errar perguntas depois de já ter subido.

---

## 3. Trilhas e Especializações por Grade

### 3.1 Trilha Frontend
- **Grade D (20–39):** HTML semântico, CSS (Flexbox/Grid), DOM, JavaScript ES6+, responsividade
- **Grade C (40–51) — escolhe Especialização:** Angular *ou* React *ou* Vue *ou* Svelte
- **Grade B (52–60):** transversal (ver seção 3.7)
- **Grade A (61–71):** aprofunda a especialização — performance de renderização, state management avançado, testes de componente, acessibilidade (a11y), SSR/SSG
- **Grade S (72+):** cross-domain (ver seção 3.8)

### 3.2 Trilha Backend
- **Grade D:** lógica de servidor, HTTP, APIs REST básicas, bancos de dados relacionais (SQL básico)
- **Grade C — Especialização:** Node.js *ou* Java/Spring *ou* .NET *ou* Python/Django *ou* PHP/Laravel
- **Grade B:** transversal
- **Grade A:** autenticação/autorização avançada, filas e mensageria, cache, escalabilidade, arquitetura de microsserviços
- **Grade S:** cross-domain

### 3.3 Trilha DevOps
- **Grade D:** terminal/Linux básico, redes básicas, conceitos de nuvem
- **Grade C — Especialização:** Cloud (AWS *ou* Azure *ou* GCP) *ou* Containers/Orquestração (Docker/Kubernetes)
- **Grade B:** transversal
- **Grade A:** IaC (Terraform), observabilidade, segurança de infraestrutura, estratégias de deploy (blue-green, canary)
- **Grade S:** cross-domain

### 3.4 Trilha Dados
- **Grade D:** fundamentos de dados, SQL básico, planilhas, estatística básica
- **Grade C — Especialização:** Engenharia de Dados (ETL/pipelines) *ou* Análise de Dados/BI *ou* Machine Learning
- **Grade B:** transversal
- **Grade A:** modelagem de data warehouse, dados em tempo real (streaming), MLOps, governança de dados
- **Grade S:** cross-domain

### 3.5 Trilha QA/Segurança
- **Grade D:** fundamentos de testes, tipos de teste, bugs e reporting
- **Grade C — Especialização:** Automação de Testes (Cypress/Playwright/Selenium) *ou* Segurança/Pentest básico
- **Grade B:** transversal
- **Grade A:** testes de performance/carga, segurança ofensiva avançada, testes em pipelines de CI/CD
- **Grade S:** cross-domain

### 3.6 Trilha Fullstack
- **Grade D:** um pouco de front + back, sem framework ainda
- **Grade C — Especialização:** escolhe uma dupla (ex: Angular + Node, React + .NET) — sempre uma combinação front + back
- **Grade B:** transversal
- **Grade A:** integração entre camadas, comunicação front-back, autenticação end-to-end, performance full-stack
- **Grade S:** cross-domain

### 3.7 Conteúdo do Grade B (transversal, todas as trilhas)
Ferramentas que todo profissional pleno precisa dominar, independente da trilha:
- Git avançado (rebase, resolução de conflitos, git flow)
- Docker básico/intermediário
- CI/CD (pipelines, conceitos de build/deploy)
- Code review e boas práticas de colaboração
- Versionamento semântico e changelogs

### 3.8 Conteúdo do Grade S (cross-domain, todas as trilhas)
Nível sênior/arquiteto — a pergunta deixa de ser "como fazer X" e passa a ser "qual a melhor decisão":
- System design (trade-offs de arquitetura)
- Decisões de escala (monolito vs microsserviços, SQL vs NoSQL)
- Comunicação entre camadas (como frontend, backend, dados e infra se conectam num sistema real)
- Liderança técnica e mentoria (perguntas situacionais/comportamentais técnicas)

---

## 4. Regras de XP

### 4.1 Ganho de XP por resposta

| Dificuldade da pergunta | XP base |
|---|---|
| Fácil | 10 XP |
| Média | 25 XP |
| Difícil | 50 XP |
| Elite (Boss Question, fim de grade) | 100 XP |

### 4.2 Multiplicadores
- **Combo Streak:** a cada 5 acertos consecutivos, +10% de XP (cap +50% aos 25 seguidos). Errar zera o combo.
- **Bônus de Descanso:** primeira resposta correta do dia em cada tema rende XP em dobro.
- **Penalidade de erro:** não remove XP acumulado; zera o combo e reduz 5% da barra de progresso do nível atual (nunca gera downgrade de nível).

### 4.3 Curva de nível por grade
- Newbie (1–19): curva linear, progressão rápida (ambientação).
- D (20–39): curva levemente quadrática.
- C (40–51): quadrática — exige prática na especialização escolhida.
- B (52–60): linear, mas com Boss Questions mais frequentes (ferramentas do dia a dia).
- A (61–71): exponencial — precisa de Duelos e Dungeons para XP relevante.
- S (72+): pós-grade máximo, XP vira **prestígio** (títulos e cosméticos, sem "nível final" fixo).

---

## 5. Regras de Quest de Grade

- Ao atingir o nível mínimo do próximo grade, o sistema libera a **Quest de Grade**: bateria de 15–20 perguntas cronometradas (mistura do conteúdo do grade atual, mais pesado nos temas de Boss Question).
- Taxa mínima de acerto para passar: 80% (ajustável por configuração de dificuldade da plataforma).
- Falhar: cooldown de 24h, sem perda de XP.
- Passar: libera oficialmente o próximo grade e, se aplicável, a tela de escolha de Trilha (Grade D) ou Especialização (Grade C).

---

## 6. Equipamentos (Cosméticos, por Grade)

Os itens seguem a nomenclatura de grade do próprio L2 — refletem em qual grade o usuário está ou já passou, sem dar vantagem nas respostas.

| Grade do item | Slot exemplo | Como adquirir |
|---|---|---|
| **No-grade** | "Vestimenta de Aprendiz" | Automático ao completar o Grade Newbie |
| **D-grade** | "Manto D da Trilha [X]" | Completar a Quest de Grade D |
| **C-grade** | "Emblema C de [Especialização]" | Completar a Quest de Grade C |
| **B-grade** | "Ferramenta B Universal" (ex: martelo do Git) | Completar a Quest de Grade B |
| **A-grade** | "Armadura A de [Especialização]" | Completar a Quest de Grade A |
| **S-grade** | "Relíquia S do Arquiteto" | Completar a Quest de Grade S |

### 6.1 Itens especiais (utilitários, não cosméticos)
- **Poção do Esquecimento**: reset único de Trilha ou Especialização.
- **Pergaminho de Segunda Chance**: pula o cooldown de 24h de uma Quest de Grade (1 uso/mês, via evento).
- **Sino da Guilda**: ativa XP em dobro para o clã inteiro por 1h (cooldown semanal).

### 6.2 Moeda interna — Adena Digital
- Obtida em dungeons diárias e desafios semanais.
- Usada só na loja de cosméticos — nunca compra XP, respostas ou dicas.

---

## 7. Continentes Temáticos (Mapa/Mundo)

Cada Trilha tem seu continente; dentro dele, "regiões" representam os grades D, C, A percorridos nessa trilha.

1. **Vale da Sintaxe** — zona Newbie, todas as trilhas passam por aqui
2. **Floresta dos Componentes** — Trilha Frontend
3. **Câmaras Sombrias do Servidor** — Trilha Backend
4. **Desfiladeiro dos Pipelines** — Trilha DevOps
5. **Minas de Dados** — Trilha Dados
6. **Cidadela da Quality Gate** — Trilha QA/Segurança
7. **Planície do Full-Stack** — Trilha Fullstack
8. **Platô das Ferramentas Universais** — zona do Grade B (todas as trilhas se cruzam aqui)
9. **Torre do Arquiteto** — zona do Grade S, endgame, dungeons cross-domain
10. **Arena da Olimpíada Técnica** — zona de PvP (Mock Interview Duels)

---

## 8. Regras de PvP — Mock Interview Duel

- Matchmaking por Grade (só duela quem está no mesmo grade, evitando desbalanceamento entre Newbie e S).
- Set de 10 perguntas idêntico para ambos, 30s por pergunta.
- Vitória por mais acertos; empate desempatado por tempo total.
- Temporadas de 3 meses, ranking reseta, recompensas exclusivas (título + cosmético sazonal) para o Top 10%.

---

## 9. Regras de Guilda/Clã

- Grupos de 5 a 50 usuários.
- Ranking semanal por XP total do clã.
- Top 3 semanal ganha aura cosmética temporária + Adena bônus para todos os membros.

---

*Documento vivo — sujeito a expansão conforme novas trilhas, dungeons e eventos sazonais forem definidos.*
