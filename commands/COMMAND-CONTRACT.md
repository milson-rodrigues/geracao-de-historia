# Command Router Contract

**Versão:** 0.1.0  
**Estado:** contrato lógico/documental.  
**Índice:** [COMMAND-INDEX.md](COMMAND-INDEX.md)  
**Manual:** [COMMAND-MANUAL.md](COMMAND-MANUAL.md)

## 1. Objetivo

Definir como uma solicitação conversacional é classificada, validada e encaminhada para uma bridge, workflow, skill e provider sem acoplar o comando a um fornecedor específico.

## 2. Pipeline lógico

```text
User Request
  -> Command Parser / Intent Resolver
  -> Command Registry
  -> Request Normalizer
  -> Policy & Input Gate
  -> Creative Orchestrator
  -> Bridge
  -> Workflow
  -> Skill Resolver
  -> Provider Capability Resolver
  -> Provider Adapter
  -> Asset Result
  -> Quality Assurance
  -> Delivery & Audit Record
```

A sequência é uma arquitetura-alvo, não uma implementação já disponível.

## 3. Responsabilidades

| Componente | Responsabilidade |
|---|---|
| Command Parser | Reconhecer comando canônico, alias e argumentos |
| Command Registry | Resolver metadados e versão do comando |
| Request Normalizer | Normalizar briefing para schema comum |
| Policy/Input Gate | Validar consentimento, direitos, fontes e requisitos obrigatórios |
| Creative Orchestrator | Planejar workflow e dependências |
| Bridge | Aplicar contrato do domínio de mídia |
| Workflow | Ordenar etapas de uma tarefa |
| Skill Resolver | Carregar skills pertinentes e verificar procedência/versão |
| Capability Resolver | Selecionar provider por capacidade e restrições |
| Provider Adapter | Traduzir contrato interno para API/CLI concreta |
| Quality Assurance | Validar o ativo segundo critérios do domínio |
| Delivery/Audit | Entregar resultado e registrar evidências |

## 4. Contrato mínimo de um comando

Cada comando registrado deve declarar:
- `id`: identificador estável;
- `canonical_name`: nome canônico com barra;
- `aliases`: aliases sem duplicar implementação;
- `bridge`: domínio proprietário;
- `intent`: ação pretendida;
- `input_schema`: referência ao schema de entrada;
- `workflow`: workflow acionado;
- `skills`: skills requeridas ou opcionais;
- `provider_capabilities`: capacidades necessárias, não um fornecedor fixo;
- `validation_profile`: critérios de QA;
- `status`: estado de implementação;
- `version`: versão do contrato.

## 5. Resolução de providers

Selecionar provider somente após identificar:
1. modalidade e subtipo da tarefa;
2. entradas disponíveis e suas funções;
3. requisitos de saída (duração, dimensões, proporção, codec, alpha, stems etc.);
4. capacidade e schema atuais do provider;
5. disponibilidade/autenticação/permissão;
6. custo/limites quando conhecidos e relevantes;
7. política de conteúdo, privacidade e consentimento.

A ordem de preferência não deve ser codificada como verdade permanente. Defaults de modelos registrados em skills externas devem ser revalidados contra documentação e schema atuais antes de uso.

Se não houver provider disponível, retornar `BLOCKED` com a capacidade ausente. Não alegar que um provider foi acionado se só foi consultada sua documentação.

## 6. Skill resolution

- Preferir skills internas versionadas para regras próprias e QA.
- Skills externas devem ter fonte, versão/commit, licença, data de verificação e estado de compatibilidade registrados.
- Não copiar diretórios completos de terceiros sem auditoria de licença, dependências e necessidade.
- Carregar apenas as referências necessárias para a tarefa.
- Skills não podem sobrepor fontes narrativas canônicas, contratos de template, políticas de segurança ou consentimento.
- Presença local de um arquivo não prova disponibilidade do provider ou execução da skill.

## 7. Regras de integridade e segurança

- Exigir consentimento adequado para clonagem de voz/identidade e uso de likeness quando aplicável.
- Não enviar arquivos sensíveis a provider externo sem base e autorização apropriadas.
- Não instalar CLI, extensões, dependências ou credenciais sem autorização quando houver alteração de ambiente/custo/permissão.
- Não executar ações irreversíveis, publicação ou gasto externo sem autorização apropriada.
- Preservar fontes canônicas e ativos aprovados.
- Manter rastreabilidade do prompt, entradas, provider/modelo, parâmetros, resultado e QA sem registrar segredos.

## 8. Evolução

Alterações no contrato devem atualizar o índice, manual, schema, registry e testes afetados. Mudanças no `ROUTER-MESTRE.md` exigem autorização explícita, conforme governança do repositório.
