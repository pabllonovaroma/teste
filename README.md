# EMA CRM v1.6

CRM comercial para prospecção, empresas, contatos, pipeline, atividades, follow-ups, propostas, parceiros, indicações, metas, relatórios, usuários e auditoria.

## Requisitos

- Node.js 24.x
- npm 10+

## Instalação

```powershell
npm install
npm run dev
```

Frontend: `http://localhost:5173`

API: `http://localhost:3333`

## Credenciais iniciais

Administrador:
- `admin@ema.local`
- `admin123`

Vendedor:
- `vendedor@ema.local`
- `123456`

Altere as senhas em ambiente real.

## v1.4

- Importação de leads via Excel/CSV.
- Pré-visualização e validação.
- Identificação de duplicados.
- Distribuição automática entre vendedores.
- Atribuição fixa de leads.
- Responsável vinculado à empresa.
- Template de importação.
- Rotas e regras de importação separadas em `server/routes/prospecting.js` e `server/services/prospectingService.js`.
- Migração automática do campo `owner_id` para instalações existentes.

Veja `docs/ARCHITECTURE.md` e `docs/IMPORTACAO-LEADS.md`.


## v1.6
- Consulta automática de CNPJ pela BrasilAPI / Minha Receita.
- Preenchimento automático de dados cadastrais, endereço, telefone, e-mail, porte, atividade e situação cadastral.
- Persistência dos dados de consulta no cadastro da empresa.
- Correção do modal de importação de leads e distribuição por vendedor/gestor.
- Mantida compatibilidade com Node 24.

## Consulta de CNPJ

Na tela **Empresas**, clique em **Nova empresa**, informe o CNPJ e clique em **Consultar CNPJ**. O sistema consulta a BrasilAPI e preenche os dados cadastrais antes do salvamento.

A implementação aceita CNPJ numérico e o novo CNPJ alfanumérico de 14 posições.
