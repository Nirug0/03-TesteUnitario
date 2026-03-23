# 📤 Guia de Commit e Push - Atividade TDD

## Status Atual

Todos os arquivos já estão no **staging area** (git add .)

```
Changes to be committed:
  ✅ EVIDENCIAS.md (novo arquivo)
  ✅ resultado-testes.txt (novo arquivo)
  ✅ src/ContaBancaria/Conta.cs (modificado)
  ✅ tests/ContaBancaria.Tests/ContaTests.cs (modificado)
```

---

## 🚀 Opção 1: Commit Único (Recomendado)

### Rápido e Direto

```bash
git commit -m "Atividade TDD: Conta Bancária com 27 testes completos"
git push origin main
```

**Resultado:** Toda a atividade em um único commit bem organizado.

---

## 🔄 Opção 2: Commit Detalhado (Com Histórico TDD)

### Documento o Ciclo TDD em Detalhes

```bash
# Commit 1: Testes
git add tests/ContaBancaria.Tests/ContaTests.cs
git commit -m "red: escreve 27 testes para Conta Bancária

- 6 testes de Construtor
- 4 testes de Depositar
- 5 testes de Sacar
- 6 testes de Transferir
- 4 testes de Encerrar

Todos os testes falham (NotImplementedException)"

# Commit 2: Implementação
git add src/ContaBancaria/Conta.cs
git commit -m "green: implementa todos os métodos da Conta

Implementação dos 5 métodos:
- Construtor com validações
- Depositar com regras de validação
- Sacar com saldo insuficiente check
- Transferir com validação de ambas contas
- Encerrar com saldo zero check

Todos os 27 testes passam!"

# Commit 3: Documentação
git add EVIDENCIAS.md resultado-testes.txt
git commit -m "docs: adiciona evidências e resultado dos testes

- EVIDENCIAS.md: sumário completo da atividade
- resultado-testes.txt: saída do 'dotnet test --verbosity normal'

Atividade TDD finalizada com sucesso!"

# Push para remote
git push origin main
```

---

## 📊 Padrão de Commits Sugerido (Próximas Atividades)

```
red:       escreve testes que falham
green:     implementa código mínimo para passar
refactor:  melhora código mantendo testes verdes
test:      adiciona mais testes de cobertura
docs:      adiciona documentação ou evidências
fix:       corrige comportamento
```

---

## ✅ Checklist Final Antes de Fazer Push

- [ ] Todos os 27 testes passando (`dotnet test`)
- [ ] Arquivo `resultado-testes.txt` criado
- [ ] Arquivo `EVIDENCIAS.md` criado
- [ ] Código `Conta.cs` sem `NotImplementedException`
- [ ] Testes `ContaTests.cs` com 27 testes
- [ ] `git add .` executado
- [ ] `git status` mostra "Changes to be committed"

---

## 🎯 Comando Rápido Para Entrega

**Copie e cole este comando:**

```bash
git commit -m "Atividade TDD: Conta Bancária com 27 testes completos" && git push origin main
```

---

## 📍 Verificar Se o Push Funcionou

Após fazer push, verifique com:

```bash
# Ver último commit
git log --oneline -5

# Ver status
git status

# Deve mostrar "Your branch is up to date with 'origin/main'"
```

---

## ❓ Troubleshooting

### Se houver erro de autenticação:
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu.email@example.com"
```

### Se precisar desfazer o commit (antes do push):
```bash
git reset --soft HEAD~1
```

### Se precisar desfazer e refazer tudo:
```bash
git reset --hard
```

---

## 🎉 Pronto Para Entrega!

Após executar o comando de commit e push, sua atividade estará no repositório GitHub com:

- ✅ 27 testes implementados e passando
- ✅ Código completamente implementado
- ✅ Evidências documentadas
- ✅ Histórico de commits visível

**Atividade concluída com sucesso!** 🚀
