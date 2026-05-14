# Documentação QA Manual — Login Feature

## Projeto
QA Manual Tests — Login Validation

## Objetivo
Validar o comportamento da funcionalidade de login do sistema disponível no site Practice Test Automation.

Sistema utilizado:

- Practice Test Automation
- URL: https://practicetestautomation.com/practice-test-login/

---

# Test Scenarios

| Scenario ID | Scenario Description | Expected Result | Status |
|---|---|---|---|
| SC01 | Login com credenciais válidas | Usuário deve acessar a página logada com sucesso | PASS |
| SC02 | Login com usuário inválido | Mensagem 'Your username is invalid!' deve aparecer | PASS |
| SC03 | Login com senha inválida | Mensagem 'Your password is invalid!' deve aparecer | PASS |
| SC04 | Login com campos vazios | Mensagem 'Your username is invalid!' deve aparecer | PASS |
| SC05 | Login com espaços entre caracteres do username | Mensagem 'Your username is invalid!' deve aparecer | PASS |
| SC06 | Login com username acima do limite esperado | Mensagem 'Your username is invalid!' deve aparecer | PASS |
| SC07 | Login com caracteres especiais no username | Mensagem 'Your username is invalid!' deve aparecer | PASS |
| SC08 | Login utilizando letras maiúsculas no username | Mensagem 'Your username is invalid!' deve aparecer | PASS |

---

# Test Cases

## TC01 — Positive Login

### Scenario
SC01 — Login com credenciais válidas

### Steps
1. Open page
2. Enter username 'student'
3. Enter password 'Password123'
4. Click Submit

### Test Data
student / Password123

### Expected Result
Usuário deve acessar a página de sucesso.

### Status
PASS

---

## TC02 — Negative Username

### Scenario
SC02 — Login com usuário inválido

### Steps
1. Open page
2. Enter username 'incorrectUser'
3. Enter password 'Password123'
4. Click Submit

### Test Data
incorrectUser / Password123

### Expected Result
Mensagem 'Your username is invalid!' deve aparecer.

### Status
PASS

---

## TC03 — Negative Password

### Scenario
SC03 — Login com senha inválida

### Steps
1. Open page
2. Enter username 'student'
3. Enter password 'incorrectPassword'
4. Click Submit

### Test Data
student / incorrectPassword

### Expected Result
Mensagem 'Your password is invalid!' deve aparecer.

### Status
PASS

---

## TC04 — Empty Fields

### Scenario
SC04 — Login com campos vazios

### Steps
1. Open page
2. Leave the login and password fields blank
3. Click Submit

### Test Data
Login and password fields blank

### Expected Result
Mensagem 'Your username is invalid!' deve aparecer.

### Status
PASS

---

## TC05 — Username With Spaces

### Scenario
SC05 — Login com espaços entre caracteres do username

### Steps
1. Open page
2. Enter username 's t u d e n t'
3. Enter password 'Password123'
4. Click Submit

### Test Data
s t u d e n t / Password123

### Expected Result
Mensagem 'Your username is invalid!' deve aparecer.

### Status
PASS

---

## TC06 — Large Username

### Scenario
SC06 — Login com username acima do limite esperado

### Steps
1. Open page
2. Enter username 'aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'
3. Enter password 'Password123'
4. Click Submit

### Test Data
aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa / Password123

### Expected Result
Mensagem 'Your username is invalid!' deve aparecer.

### Status
PASS

---

## TC07 — Special Characters

### Scenario
SC07 — Login com caracteres especiais no username

### Steps
1. Open page
2. Enter username '!@#$%¨&*())'
3. Enter password 'Password123'
4. Click Submit

### Test Data
!@#$%¨&*()) / Password123

### Expected Result
Mensagem 'Your username is invalid!' deve aparecer.

### Status
PASS

---

## TC08 — Uppercase Username

### Scenario
SC08 — Login utilizando letras maiúsculas no username

### Steps
1. Open page
2. Enter username 'STUDENT'
3. Enter password 'Password123'
4. Click Submit

### Test Data
STUDENT / Password123

### Expected Result
Mensagem 'Your username is invalid!' deve aparecer.

### Status
PASS

---

# Conclusão

Todos os cenários executados durante a validação manual da funcionalidade de login apresentaram o comportamento esperado.

Os testes contemplaram:

- Testes positivos
- Testes negativos
- Edge cases
- Validação de input
- Sensibilidade de caracteres
- Campos vazios
- Caracteres especiais
- Boundary testing

---


