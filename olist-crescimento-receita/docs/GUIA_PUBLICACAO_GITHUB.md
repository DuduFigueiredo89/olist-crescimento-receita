# Publicação e entrega acadêmica — Olist Crescimento e Receita

## Criar o repositório

1. Em https://github.com/new, crie o repositório `olist-crescimento-receita`.
2. Escolha **Public** caso a banca precise consultar os arquivos pelo link.
3. Não selecione a criação automática de README ou `.gitignore` (já estão no projeto).
4. Copie o endereço HTTPS do repositório.

## Publicação pelo VS Code

Abra a **pasta deste projeto**, separada de `olist-customer-analytics`. No PowerShell:

```powershell
git init
git branch -M main
git add .
git commit -m "Entrega acadêmica: Olist Crescimento e Receita"
git remote add origin https://github.com/DuduFigueiredo89/olist-crescimento-receita.git
git push -u origin main
```

Se já existir um diretório `.git`, execute `git remote -v` antes de configurar `origin`; não substitua o remoto do projeto anterior.

## Checklist de submissão

- [ ] Notebook `01_crescimento_receita.ipynb` executa integralmente sem erros.
- [ ] A planilha contém as abas `Decomposicao`, `Cenarios`, `Sensibilidade`, `Priorizacao_UF`, `Robustez` e `Plano_90d`.
- [ ] Pedidos jan–ago/2018: 52.783. GMV do mesmo período: R$ 7.218.125,12.
- [ ] Conferidas as 15 figuras e atualizadas as saídas em `outputs/`.
- [ ] Relatório PDF, apresentação e notebook mostram as mesmas métricas e definições.
- [ ] Nenhum dado sensível, `.venv/` ou arquivo de acesso foi incluído no commit.
- [ ] Link do repositório e arquivos de apresentação foram inseridos na entrega da pós-graduação.

**Nota metodológica:** os dados Olist são históricos. GMV não é lucro nem receita reconhecida; os cenários são simulações condicionais e a triagem regional não demonstra rentabilidade.
