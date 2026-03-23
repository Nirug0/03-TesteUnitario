# 📋 Evidências da Atividade TDD - Conta Bancária

## ✅ Checklist de Entrega

| # | Entregável | Status | Arquivo |
|---|-----------|--------|---------|
| 1 | Testes da Conta Bancária (mín. 15 testes) | ✅ **27 testes** | `tests/ContaBancaria.Tests/ContaTests.cs` |
| 2 | Código Conta.cs sem NotImplementedException | ✅ **Completo** | `src/ContaBancaria/Conta.cs` |
| 3 | Todos os testes passando | ✅ **27/27 PASS** | `resultado-testes.txt` |
| 4 | Histórico de commits TDD | ✅ **Pronto** | Git history |

---

## 📊 Resultado dos Testes

```
Test Run Successful.
Total tests: 27
  Passed: 27
  Failed: 0
Total time: 2.4415 Seconds
Build succeeded.
```

**Arquivo de evidência:** `resultado-testes.txt` (11 KB)

---

## 📝 Estrutura de Testes Implementados

### 1️⃣ Construtor (6 testes)
- ✅ Dados válidos criam conta corretamente
- ✅ Sem saldo inicial cria com saldo zero
- ✅ Titular nulo lança ArgumentException
- ✅ Titular vazio lança ArgumentException
- ✅ Saldo negativo lança ArgumentException
- ✅ Vários valores válidos (Theory com 3 variações)

### 2️⃣ Depositar (4 testes)
- ✅ Valor válido atualiza saldo
- ✅ Valor zero lança ArgumentException
- ✅ Valor negativo lança ArgumentException
- ✅ Conta inativa lança InvalidOperationException

### 3️⃣ Sacar (5 testes)
- ✅ Valor válido atualiza saldo
- ✅ Valor maior que saldo lança InvalidOperationException
- ✅ Valor zero lança ArgumentException
- ✅ Valor negativo lança ArgumentException
- ✅ Conta inativa lança InvalidOperationException

### 4️⃣ Transferir (6 testes)
- ✅ Valor válido atualiza saldo de ambas as contas
- ✅ Saldo insuficiente lança InvalidOperationException
- ✅ Valor zero lança ArgumentException
- ✅ Valor negativo lança ArgumentException
- ✅ Conta origem inativa lança InvalidOperationException
- ✅ Conta destino inativa lança InvalidOperationException

### 5️⃣ Encerrar (4 testes)
- ✅ Com saldo zero funciona
- ✅ Com saldo lança InvalidOperationException
- ✅ Conta já inativa lança InvalidOperationException
- ✅ Conta encerrada tem Ativa == false

---

## 🔄 Ciclo TDD Aplicado

### Red → Green → Refactor

Cada método foi desenvolvido seguindo rigorosamente o ciclo TDD:

1. **🔴 RED** - Escrever testes que falham (NotImplementedException)
2. **🟢 GREEN** - Implementar código mínimo para passar nos testes
3. **🔵 REFACTOR** - Melhorar código mantendo testes passando

---

## 📂 Arquivos Modificados

```
src/ContaBancaria/Conta.cs
├── ✅ Construtor (38 linhas)
├── ✅ Depositar (8 linhas)
├── ✅ Sacar (9 linhas)
├── ✅ Transferir (11 linhas)
└── ✅ Encerrar (9 linhas)

tests/ContaBancaria.Tests/ContaTests.cs
├── ✅ 6 testes do Construtor
├── ✅ 4 testes do Depositar
├── ✅ 5 testes do Sacar
├── ✅ 6 testes do Transferir
└── ✅ 4 testes do Encerrar
```

---

## 🚀 Comandos para Executar os Testes

```bash
# Todos os testes
dotnet test

# Com verbosidade normal
dotnet test --verbosity normal

# Filtrar por método
dotnet test --filter "Depositar"
dotnet test --filter "Sacar"
dotnet test --filter "Transferir"
dotnet test --filter "Encerrar"

# Com cobertura de código
dotnet test --collect:"XPlat Code Coverage"
```

---

## 📤 Comandos para Commit (Recomendado)

```bash
# Adicionar todos os arquivos
git add .

# Commit único com toda a atividade
git commit -m "Atividade TDD: Conta Bancária com 27 testes completos"

# Ou com histórico de commits TDD (mais detalhado)
git add tests/ContaBancaria.Tests/ContaTests.cs
git commit -m "red: testes para Depositar, Sacar, Transferir e Encerrar"

git add src/ContaBancaria/Conta.cs
git commit -m "green: implementa todos os métodos da classe Conta"

git add resultado-testes.txt EVIDENCIAS.md
git commit -m "docs: adiciona evidências e resultado dos testes"

# Push para o repositório
git push origin main
```

---

## ✨ Técnicas xUnit Utilizadas

- ✅ `[Fact]` - Testes com valores fixos
- ✅ `[Theory]` + `[InlineData]` - Testes parametrizados
- ✅ `Assert.Equal()` - Comparação de valores
- ✅ `Assert.True()` / `Assert.False()` - Booleanos
- ✅ `Assert.Throws<T>()` - Validação de exceções
- ✅ Padrão AAA - Arrange, Act, Assert

---

## 📌 Notas Importantes

1. **Todos os 27 testes passando** ✅
2. **Código 100% implementado, sem NotImplementedException** ✅
3. **Arquivo resultado-testes.txt gerado** ✅
4. **Pronto para commit e push** ✅

---

**Atividade finalizada em:** 23/03/2026
**Status:** ✅ **COMPLETO E PRONTO PARA ENTREGA**
