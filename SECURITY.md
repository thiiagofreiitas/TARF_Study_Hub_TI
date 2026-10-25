# Política de Segurança – PortfolioHUB

Este documento descreve as práticas de segurança adotadas no **PortfolioHUB** (`TARF_Study_Hub_TI`), repositório de portfólio acadêmico de THIAGO FREITAS, estudante de Análise e Desenvolvimento de Sistemas (ADS).

## 1. Escopo

Esta política vale para todo o conteúdo do repositório: documentos, códigos, anotações, projetos e o site publicado via GitHub Pages.

## 2. Versões suportadas

| Versão | Suporte |
|--------|---------|
| Branch `main` (versão publicada) | ✅ Recebe correções de segurança |
| Branches de desenvolvimento | ❌ Sem suporte |

## 3. Como reportar uma vulnerabilidade

Se você encontrar algum problema de segurança (por exemplo, dado sensível exposto, link malicioso ou falha no site):

1. **Não divulgue publicamente** o problema antes de ele ser corrigido.
2. Entre em contato por um destes canais:
   - E-mail: thiiagofreiitas@sempreceub.com
   - GitHub: aba **Security → Report a vulnerability**, se estiver habilitada
3. Informe na mensagem:
   - descrição do problema;
   - onde ele ocorre (arquivo, link ou página);
   - passos para reproduzir;
   - impacto estimado.

**Prazos (compromisso de boa-fé):**
- Confirmação de recebimento em até **5 dias úteis**;
- Correção ou resposta com plano de ação em até **15 dias úteis**.

## 4. Políticas de segurança implementadas

### 4.1 Contas e autenticação
- Autenticação em dois fatores (2FA) ativada na conta do proprietário.
- Senha forte e exclusiva para o GitHub.
- Uso de HTTPS para clonar e enviar código; se usar SSH, as chaves ficam apenas no computador pessoal.

### 4.2 Gestão de usuários e permissões
- **Princípio do menor privilégio:** cada pessoa recebe apenas o acesso necessário.
- Perfis:

| Perfil | Permissão | Quem |
|--------|-----------|------|
| Proprietário | Admin | Autor do repositório |
| Colaborador | Write (somente via pull request) | Pessoas convidadas, como colegas ou professor |
| Visitante | Leitura pública | Qualquer pessoa, via GitHub Pages |

- Os acessos são revisados periodicamente, e colaboradores que não precisam mais de acesso são removidos.

### 4.3 Proteção do código
- Branch `main` protegida: alterações somente por **pull request**, com revisão antes do merge.
- Push direto na `main` e *force push* desativados.
- Histórico de commits mantido para rastreabilidade.

### 4.4 Proteção de dados e segredos
- **Nunca** versionar senhas, tokens, chaves de API, documentos pessoais ou dados de terceiros.
- Arquivos locais e de configuração listados no `.gitignore`.
- **Secret scanning** ativado para detectar segredos enviados por engano.
- Antes de cada commit, revisar os arquivos incluídos (`git status` e `git diff`).

### 4.5 Dependências
- **Dependabot** ativado para alertas de dependências vulneráveis, quando aplicável.
- Dependências desatualizadas são revisadas e atualizadas.

### 4.6 Conteúdo publicado
- Somente conteúdo próprio ou com autoria devidamente citada.
- Dados pessoais exibidos publicamente limitados ao necessário (nome, links profissionais e contato).
- Links externos conferidos antes da publicação.

## 5. Se um segredo for exposto

1. **Revogue ou troque** imediatamente a credencial exposta.
2. Remova o segredo do repositório e, se necessário, limpe o histórico.
3. Verifique se houve uso indevido.
4. Registre o ocorrido e o que foi feito para evitar repetição.

> Apagar o arquivo em um novo commit **não é suficiente**, porque o segredo continua no histórico. A prioridade é sempre revogar a credencial.

## 6. Uso responsável de IA

O Google Gemini é usado como apoio para revisar boas práticas e planejar a implantação. Nenhum segredo, senha ou dado pessoal sensível é enviado a ferramentas de IA, e as sugestões recebidas são validadas antes de serem aplicadas.

## 7. Boas práticas de colaboração

- Uma branch por tarefa, com nomes claros (ex.: `feature/disciplina-logica`).
- Commits pequenos e descritivos.
- Pull requests com descrição e revisão.
- Detalhes do fluxo em [`CONTRIBUTING.md`](CONTRIBUTING.md).

## 8. Checklist de segurança

- [ ] 2FA ativado
- [ ] Branch `main` protegida
- [ ] `.gitignore` configurado
- [ ] Secret scanning ativado
- [ ] Dependabot ativado
- [ ] Colaboradores revisados
- [ ] Nenhum dado sensível no repositório
- [ ] `SECURITY.md` publicado na raiz

## 9. Contato

- **Responsável:** Thiago Freitas
- **E-mail:** thiiagofreiitas@sempreceub.com
- **GitHub:** thiiagofreiitas
- **LinkedIn:** thiiagofreiitas

---

*Última atualização: 25/10/2026*
