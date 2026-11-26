# Capitaly

Plataforma SaaS de gestão financeira pessoal com inteligência artificial. O usuário organiza a vida financeira em um só lugar e, no plano Premium, conversa com a Capitaly AI para analisar seus dados e cadastrar informações por comando de texto.

Projeto interdisciplinar de Engenharia de Software II e Programação em Scripts (Fatec São Caetano do Sul).

## Funcionalidades

- Receitas e despesas com categorias
- Controle de dívidas, com juros, parcelas e vencimento
- Investimentos e rentabilidade
- Metas financeiras com prazo e progresso
- Gestão de veículo
- Capitaly AI (Premium): análise financeira e cadastro de dívidas, lançamentos, investimentos e metas por conversa
- Painel administrativo para gerenciar usuários e planos
- Dois planos: Normal (R$ 19,90/mês) e Premium (R$ 39,90/mês), com checkout simulado

## Tecnologias

- Frontend: HTML, CSS e JavaScript puro
- Backend: PHP 8.1+
- Banco de dados: MySQL
- IA: API do Google Gemini, chamada somente pelo servidor

## Segurança

- Senhas com bcrypt (`password_hash`)
- Prepared statements em todas as consultas
- Dados isolados por usuário
- Validação no frontend e no servidor
- Cookie de sessão HttpOnly/SameSite e proteção CSRF por cabeçalho
- Chave da IA mantida apenas no servidor

## Como rodar (XAMPP)

1. Copie a pasta `capitaly` para `C:\xampp\htdocs\`.
2. Inicie o Apache e o MySQL no XAMPP.
3. No phpMyAdmin, importe o `capitaly.sql`. Atenção: ele apaga e recria as tabelas do banco `capitaly`.
4. Defina a variável de ambiente `GEMINI_API_KEY` com a sua chave (gratuita em https://aistudio.google.com).
5. Acesse `http://localhost/capitaly/`.

Para conferir o ambiente, abra `http://localhost/capitaly/api/diagnostico.php`.
Se o seu MySQL usar senha ou porta diferentes, ajuste as variáveis `CAPITALY_DB_*` ou o `api/config.php`.

## Equipe

- Gabriel de Almeida Mazur
- Guilherme Santos Souza

Orientação: Prof. Humberto Luiz de Toledo
