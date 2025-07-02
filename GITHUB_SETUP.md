# Configuração do GitHub

> Este guia é voltado para os mantenedores do repositório e pessoas responsáveis pela moderação e estrutura técnica do projeto no GitHub.

Este documento contém instruções para configurar adequadamente o repositório no GitHub.

## 1. Ativar GitHub Discussions

### Passos:
1. Vá para o repositório no GitHub
2. Clique em **Settings** (Configurações)
3. Role para baixo até a seção **Features**
4. Marque a caixa **Discussions**
5. Clique em **Save**

### Categorias Sugeridas para Discussions:
- **📢 Anúncios**: Informações importantes sobre o evento
- **💡 Ideias**: Sugestões para palestras, workshops e atividades
- **🤝 Networking**: Conexões entre participantes e palestrantes
- **❓ Perguntas**: Dúvidas sobre o evento ou proposta
- **🎯 Organização**: Discussões sobre logística e planejamento

## 2. Configurar Templates de Issue

Certifique-se de criar o diretório `.github/ISSUE_TEMPLATE/` se ele ainda não existir.

### Template para Sugestões:
Crie um arquivo `.github/ISSUE_TEMPLATE/sugestao.md`:

```markdown
---
name: Sugestão
about: Sugira uma ideia para o evento
title: '[SUGESTÃO] '
labels: 'sugestao'
assignees: ''
---

## Descrição da Sugestão
[Descreva sua sugestão de forma clara e concisa]

## Tipo de Sugestão
- [ ] Tema de palestra
- [ ] Workshop
- [ ] Palestrante
- [ ] Atividade de networking
- [ ] Melhoria na proposta
- [ ] Outro

## Justificativa
[Explique por que esta sugestão seria benéfica para o evento]

## Informações Adicionais
[Qualquer informação adicional que possa ajudar]
```

### Template para Dúvidas:
Crie um arquivo `.github/ISSUE_TEMPLATE/duvida.md`:

```markdown
---
name: Dúvida
about: Faça uma pergunta sobre o evento
title: '[DÚVIDA] '
labels: 'duvida'
assignees: ''
---

## Sua Dúvida
[Descreva sua dúvida de forma clara]

## Contexto
[Forneça contexto adicional se necessário]

## O que você já tentou
[Se aplicável, descreva o que você já tentou]
```

## 3. Configurar Templates de Pull Request

Crie um arquivo `.github/pull_request_template.md`:

> O GitHub detecta automaticamente este arquivo para preenchimento automático de novos PRs.

```markdown
## Descrição
[Descreva as mudanças feitas]

## Tipo de Mudança
- [ ] Correção de bug
- [ ] Nova funcionalidade
- [ ] Melhoria na documentação
- [ ] Outro

## Checklist
- [ ] Minhas mudanças seguem o estilo do projeto
- [ ] Testei minhas mudanças localmente
- [ ] Atualizei a documentação conforme necessário

## Informações Adicionais
[Qualquer informação adicional relevante]
```

## 4. Configurar Labels

Crie as seguintes labels no repositório:

### Labels para Issues:
- `sugestao` (azul) - Sugestões para o evento
- `duvida` (amarelo) - Dúvidas sobre o projeto
- `bug` (vermelho) - Problemas encontrados
- `melhoria` (verde) - Melhorias na documentação
- `urgente` (vermelho escuro) - Questões urgentes

### Labels para Pull Requests:
- `documentacao` (azul claro) - Mudanças na documentação
- `correcao` (verde) - Correções de texto
- `revisao` (laranja) - Precisa de revisão

## 5. Configurar Branch Protection

1. Vá para **Settings** > **Branches**
2. Clique em **Add rule**
3. Configure para a branch `main`:
   - ✅ Require pull request reviews before merging
   - ✅ Require status checks to pass before merging
   - ✅ Include administrators

## 6. Configurar Páginas do GitHub (Opcional)

Para criar um site do projeto:

1. Vá para **Settings** > **Pages**
2. Selecione **Deploy from a branch**
3. Escolha a branch `main` e pasta `/docs`
4. Salve as configurações

## 7. Configurar Segurança

1. Vá para **Settings** > **Security**
2. Ative **Dependency graph**
3. Configure **Dependabot alerts** se aplicável

## 8. Configurar Integrações (Opcional)

- **Slack**: Para notificações de issues e PRs
- **Discord**: Para integração com servidor da comunidade
- **Email**: Para notificações por email

## ✅ Checklist Final

- [ ] GitHub Discussions ativado
- [ ] Templates de Issue e PR configurados
- [ ] Labels criadas e atribuídas
- [ ] Proteção da branch `main` ativa
- [ ] Página GitHub Pages (se aplicável)
- [ ] Alertas de segurança ativados
- [ ] Integrações conectadas (Slack/Discord)

---

*Após configurar estas opções, o repositório estará pronto para receber contribuições da comunidade de forma organizada e eficiente.*
