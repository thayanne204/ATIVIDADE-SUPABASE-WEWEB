# ATIVIDADE-SUPABASE-WEWEB
PROJETO FINAL 

# EventFlow — Sistema de Eventos (Supabase + WeWeb)

## Descrição
Aplicação para gerenciar eventos, ingressos e inscrições. Implementada com Supabase (back-end e banco de dados PostgreSQL) e WeWeb (front-end low-code). Projeto para disciplina: INTEGRAÇÃO DE BANCO DE DADOS- Integração Supabase + WeWeb.

## Funcionalidades
- CRUD completo para Eventos e Tickets.
- Registro/compra de ingressos (Registrations).
- View `view_upcoming_events` mostrando eventos futuros e disponibilidade.
- Função `get_event_sales(event_uuid)` para resumo de vendas (receita e ingressos vendidos).
- Autenticação (opcional): Supabase Auth (Google/GitHub).

## Modelo lógico
Tabelas: `users`, `categories`, `venues`, `events`, `tickets`, `registrations`.
Relações: `events` -> `categories`, `events` -> `venues`, `tickets` -> `events`, `registrations` -> `tickets` & `users`.

## Como rodar (deploy)
1. Criar projeto no Supabase.
2. Rodar SQL no SQL Editor (arquivo `db/schema.sql`) — cria tabelas, view e função.
3. Criar as policies de RLS se desejar segurança (ex.: apenas organizadores podem criar eventos).
4. Conectar WeWeb ao Supabase (URL + ANON KEY) e criar páginas conforme pasta `weweb/`.
5. Publicar no WeWeb e adicionar link no README.

## Estrutura do repositório
- `db/schema.sql` — SQL de criação do banco (tabelas, view, função, triggers).
- `weweb/` — instruções e prints das telas (export ou imagens).
- `docs/` — modelo lógico (imagem), roteiro do vídeo, prints.
- `README.md` — este arquivo.
