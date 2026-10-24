# Skills e recursos — roteamento oficial

**Versão:** 1.0.0  
**Escopo:** roteamento da geração e avaliação das pranchas infantis.

## 1. Skill principal — geração de imagem

- Repositório: https://github.com/higgsfield-ai/skills
- Skill: [`higgsfield-generate/SKILL.md`](https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md)
- Cópia presente neste repositório: [`.agents/skills/higgsfield-generate/SKILL.md`](../.agents/skills/higgsfield-generate/SKILL.md)

**Obrigatória como primeira escolha para geração**, quando de fato disponível. Antes de cada execução que gere imagem, abra a versão atual da skill externa na branch `main` ou use a cópia local se a consulta externa estiver indisponível e a rota permitir; registre qual fonte foi realmente lida. Não afirme que a skill foi executada só porque existe no repositório.

Verifique se o ambiente tem a ferramenta/CLI necessária, acesso, autenticação e suporte ao parâmetro de quantidade. Não instale, execute nem suponha ferramentas ou credenciais sem evidência e autorização. Nunca exponha segredos.

## 2. Skill complementar — direção artística

- [taste-skill](https://github.com/Leonxlnx/taste-skill)

Consultar quando for útil avaliar hierarquia visual, composição, paleta e acabamento. Não pode contrariar o texto bíblico oficial, o prompt do projeto, as imagens aprovadas ou as regras de qualidade infantil. O link não comprova instalação ou disponibilidade.

## 3. Skill opcional — exploração visual

- [open-design](https://github.com/nexu-io/open-design)

Usar somente quando a tarefa justificar exploração ou organização visual. Não é requisito por história e não substitui a skill principal.

## 4. Ordem de precedência

1. Narrativa oficial da história e identidade narrativa bloqueada.
2. Estado de produção e autorização para iniciar.
3. Rota e prompt oficiais do projeto.
4. Skill principal de geração, se disponível.
5. Referências visuais aprovadas.
6. Skills complementares, sem contrariar as regras acima.

## 5. Evidência mínima

Ao terminar, informar: skill/documento realmente consultado; ferramenta real utilizada; quantidade configurada quando houver controle; quantidade de imagens retornada; limitações e resultado da validação. Se a skill ou ferramenta não estiver acessível, parar ou seguir apenas a alternativa explicitamente permitida, informando a limitação. Não alegar instalação, chamada, salvamento ou validação sem evidência.
