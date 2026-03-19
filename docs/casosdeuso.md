# Documento de Casos de Uso — Sistema Acadêmico

## Atores

- Aluno  
- Professor  
- Secretaria Acadêmica  
- Coordenador  
- Financeiro  
- Administrador  
- Gateway de Pagamento  

---

## UC01 — Realizar Login

**Ator Principal**  
Usuário

**Objetivo**  
Permitir acesso ao sistema.

**Pré-condições**
- Usuário cadastrado.

**Pós-condições**
- Usuário autenticado.

**Fluxo Principal**
1. Usuário informa login e senha.
2. Sistema valida os dados.
3. Sistema libera acesso.

**Fluxos Alternativos**

A1 — Dados incorretos  
Sistema mostra erro.

**RF Relacionados**
- RF01 — Autenticar usuário.

**RNF Relacionados**
- RNF01 — Login em poucos segundos.

**RN Relacionadas**
- RN01 — Após 5 erros a conta pode ser bloqueada.

---<img width="661" height="777" alt="Captura de tela 2026-03-18 203850" src="https://github.com/user-attachments/assets/aea7e50b-7a35-43fa-99ea-aa3cb2404e75" />


## UC02 — Recuperar Senha

**Ator Principal**  
Usuário

**Objetivo**  
Permitir redefinir senha.

**Pré-condições**
- Usuário cadastrado.

**Pós-condições**
- Senha atualizada.

**Fluxo Principal**
1. Usuário solicita recuperação.
2. Sistema envia link ou código.
3. Usuário cria nova senha.

**Fluxos Alternativos**

A1 — Email não encontrado.
<img width="170" height="185" alt="image" src="https://github.com/user-attachments/assets/91e82e5e-6403-4e27-8b98-b7283cfa1ca0" />

---

## UC03 — Atualizar Cadastro

**Ator Principal**  
Aluno

**Objetivo**  
Atualizar dados pessoais.

**Pré-condições**
- Aluno logado.

**Pós-condições**
- Dados atualizados.

**Fluxo Principal**
1. Aluno acessa perfil.
2. Altera dados.
3. Sistema salva alterações.
<img width="208" height="223" alt="image" src="https://github.com/user-attachments/assets/13a5463d-b024-465b-820b-5cb5aa210ecf" />

---

## UC04 — Consultar Grade Horária

**Ator Principal**  
Aluno

**Objetivo**  
Ver grade de aulas.

**Pré-condições**
- Aluno logado.

**Pós-condições**
- Grade exibida.

**Fluxo Principal**
1. Aluno abre grade.
2. Sistema mostra disciplinas e horários.
<img width="206" height="193" alt="image" src="https://github.com/user-attachments/assets/767ecd31-1629-405d-989a-9d2a66d13146" />

---

## UC05 — Realizar Matrícula

**Ator Principal**  
Aluno

**Objetivo**  
Matricular disciplinas.

**Pré-condições**
- Período de matrícula aberto.

**Pós-condições**
- Matrícula registrada.

**Fluxo Principal**
1. Aluno escolhe disciplinas.
2. Sistema valida vagas e horários.
3. Matrícula confirmada.
<img width="170" height="185" alt="image" src="https://github.com/user-attachments/assets/11b28380-6a5a-4621-89d5-a6d6c2cbb879" />

---

## UC06 — Cancelar Matrícula

**Ator Principal**  
Aluno

**Objetivo**  
Cancelar disciplina.

**Pré-condições**
- Matrícula existente.

**Pós-condições**
- Disciplina removida.

**Fluxo Principal**
1. Aluno seleciona disciplina.
2. Sistema confirma cancelamento.
@startuml
actor Aluno
Aluno --> (Cancelar Matricula)
@enduml
---

## UC07 — Consultar Histórico

**Ator Principal**  
Aluno

**Objetivo**  
Visualizar histórico escolar.

**Pré-condições**
- Aluno logado.

**Pós-condições**
- Histórico exibido.

**Fluxo Principal**
1. Aluno acessa histórico.
2. Sistema mostra disciplinas e notas.
<img width="175" height="187" alt="image" src="https://github.com/user-attachments/assets/98308144-94d6-4b37-836c-987c48f0b970" />

---

## UC08 — Emitir Declaração

**Ator Principal**  
Aluno

**Objetivo**  
Gerar declaração de matrícula.

**Pré-condições**
- Matrícula ativa.

**Pós-condições**
- Documento gerado.

**Fluxo Principal**
1. Aluno solicita documento.
2. Sistema gera PDF.
<img width="169" height="185" alt="image" src="https://github.com/user-attachments/assets/1c993169-2ba4-431f-8272-109f671f5dee" />

---

## UC09 — Solicitar Aproveitamento

**Ator Principal**  
Aluno

**Objetivo**  
Solicitar equivalência de disciplina.

**Pré-condições**
- Aluno logado.

**Pós-condições**
- Solicitação registrada.

**Fluxo Principal**
1. Aluno envia pedido.
2. Sistema registra protocolo.
<img width="205" height="192" alt="image" src="https://github.com/user-attachments/assets/039d1f52-6928-472f-a0ba-843e3e414b7a" />

---

## UC10 — Lançar Frequência

**Ator Principal**  
Professor

**Objetivo**  
Registrar presença.

**Pré-condições**
- Professor logado.

**Pós-condições**
- Frequência registrada.

**Fluxo Principal**
1. Professor abre turma.
2. Marca presença.
3. Sistema salva.
<img width="176" height="187" alt="image" src="https://github.com/user-attachments/assets/cc1fdde1-729a-47e1-82ba-0172e29a2c5e" />

---

## UC11 — Lançar Notas

**Ator Principal**  
Professor

**Objetivo**  
Registrar notas.

**Pré-condições**
- Professor responsável pela turma.

**Pós-condições**
- Notas registradas.

**Fluxo Principal**
1. Professor insere notas.
2. Sistema salva dados.
<img width="149" height="181" alt="image" src="https://github.com/user-attachments/assets/576f4961-3b24-4a46-adc9-8357c2063f69" />

---

## UC12 — Publicar Material

**Ator Principal**  
Professor

**Objetivo**  
Enviar material para alunos.

**Pré-condições**
- Professor logado.

**Pós-condições**
- Material disponível.

**Fluxo Principal**
1. Professor envia arquivo.
2. Sistema publica na turma.

---

## UC13 — Registrar Turma

**Ator Principal**  
Secretaria

**Objetivo**  
Criar turma no sistema.

**Pré-condições**
- Disciplina cadastrada.

**Pós-condições**
- Turma registrada.

---

## UC14 — Aprovar Oferta

**Ator Principal**  
Coordenador

**Objetivo**  
Aprovar disciplinas do semestre.

**Pré-condições**
- Oferta criada.

**Pós-condições**
- Oferta liberada para matrícula.

---

## UC15 — Gerar Boletim

**Ator Principal**  
Secretaria

**Objetivo**  
Gerar boletim do aluno.

**Pré-condições**
- Notas registradas.

**Pós-condições**
- Boletim gerado.

---

## UC16 — Emitir Mensalidade

**Ator Principal**  
Financeiro

**Objetivo**  
Gerar cobrança.

**Pré-condições**
- Aluno ativo.

**Pós-condições**
- Cobrança criada.

---

## UC17 — Registrar Pagamento

**Ator Principal**  
Gateway de Pagamento

**Objetivo**  
Confirmar pagamento.

**Pré-condições**
- Cobrança existente.

**Pós-condições**
- Pagamento registrado.

---

## UC18 — Abrir Chamado

**Ator Principal**  
Aluno

**Objetivo**  
Solicitar suporte.

**Pré-condições**
- Aluno logado.

**Pós-condições**
- Chamado registrado.

---

## UC19 — Gerenciar Usuários

**Ator Principal**  
Administrador

**Objetivo**  
Administrar contas.

**Pré-condições**
- Admin logado.

**Pós-condições**
- Usuários atualizados.

---

## UC20 — Gerar Relatórios

**Ator Principal**  
Administrador

**Objetivo**  
Gerar relatórios do sistema.

**Pré-condições**
- Admin logado.

**Pós-condições**
- Relatório gerado.

  ---
  ## Diagrama Geral
  <img width="1180" height="108" alt="image" src="https://github.com/user-attachments/assets/bf2ca350-7d18-4ff2-a2a8-2033f6f1651a" />
