### Estrutura de Branches

- **main**: Código estável e pronto para produção.
- **develop**: Código em desenvolvimento, com todas as funcionalidades integradas.
- **feature branches**: Para criação de layout e desenvolvimento de novas funcionalidades.
- **review branches**: Para revisão final antes do deploy.

### Passo a Passo do Flow com Alterações na Etapa de Layout

#### 1. Criação do Layout da Home

1. **Criar Repositório**: No GitHub, criar um novo repositório chamado `institutional-website`.
2. **Clone o Repositório**:
   ```bash
   git clone https://github.com/seu-usuario/institutional-website.git
   ```
3. **Criar Develop Branch**:
   ```bash
   git checkout -b develop
   git push origin develop
   ```
4. **Criar Feature Branch para o Layout**:
   ```bash
   git checkout develop
   git checkout -b feature/home-layout
   ```
5. **Desenvolver o Layout da Home**:
   - Criar e editar `index.html`, adicionar estilos em `styles.css`, adicionar scripts em `scripts.js`.
6. **Commit das Mudanças**:
   ```bash
   git add .
   git commit -m "Create initial home layout"
   ```
7. **Push da Branch**:
   ```bash
   git push origin feature/home-layout
   ```
8. **Abrir Pull Request (PR)**:
   - No GitHub, abrir um PR de `feature/home-layout` para `develop`.
   - Descrever o layout criado e pedir revisão.
9. **Revisão e Feedback do Cliente**:
   - O time e/ou o cliente revisam o layout da Home e fornecem feedback detalhado.

#### 2. Solicitação de Alterações no Layout

1. **Receber Feedback do Cliente**:
   - O cliente fornece feedback solicitando alterações no layout da Home.
2. **Criar Feature Branch para Alterações**:
   ```bash
   git checkout develop
   git checkout -b feature/layout-adjustments
   ```
3. **Implementar as Alterações**:
   - Fazer os ajustes solicitados no `index.html`, `styles.css`, e `scripts.js`.
   - Adicionar, modificar ou remover elementos conforme feedback.
4. **Commit das Mudanças**:
   ```bash
   git add .
   git commit -m "Implement layout adjustments based on client feedback"
   ```
5. **Push da Branch**:
   ```bash
   git push origin feature/layout-adjustments
   ```
6. **Abrir Pull Request (PR)**:
   - No GitHub, abrir um PR de `feature/layout-adjustments` para `develop`.
   - Descrever as alterações feitas e pedir nova revisão.
7. **Revisão e Aprovação das Alterações**:
   - O time e/ou cliente revisam novamente as alterações e aprovam.
8. **Mesclagem das Alterações**:
   - Após aprovação, mesclar o PR na `develop`.
   ```bash
   git checkout develop
   git merge feature/layout-adjustments
   git push origin develop
   ```

#### 3. Montagem Após Aprovação do Layout

1. **Aprovação Final do Cliente**: Após o cliente aprovar as alterações no layout da Home, continuar com o processo de montagem.
2. **Criar Feature Branch para Montagem**:
   ```bash
   git checkout develop
   git checkout -b feature/montagem
   ```
3. **Desenvolver as Páginas Restantes**:
   - Criar e editar `about.html`, `services.html`, `portfolio.html`, `contact.html`, atualizar estilos e scripts.
4. **Commit das Mudanças**:
   ```bash
   git add .
   git commit -m "Add remaining pages and integrate styles and scripts"
   ```
5. **Push da Branch**:
   ```bash
   git push origin feature/montagem
   ```
6. **Abrir Pull Request (PR)**:
   - No GitHub, abrir um PR de `feature/montagem` para `develop`.
   - Descrever as páginas adicionadas e pedir revisão.
7. **Revisão e Ajustes**:
   - Realizar ajustes conforme feedback do time e/ou cliente.
8. **Mesclagem da Montagem**:
   - Após aprovação, mesclar o PR na `develop`.
   ```bash
   git checkout develop
   git merge feature/montagem
   git push origin develop
   ```

#### 4. Checklist Final

1. **Criar Review Branch para Checklist Final**:
   ```bash
   git checkout develop
   git checkout -b review/checklist-final
   ```
2. **Realizar Checklist Final**:
   - Revisar todo o código, corrigir possíveis bugs, otimizar performance, garantir responsividade.
3. **Commit das Correções**:
   ```bash
   git add .
   git commit -m "Final checklist and code review"
   ```
4. **Push da Branch**:
   ```bash
   git push origin review/checklist-final
   ```
5. **Abrir Pull Request (PR)**:
   - No GitHub, abrir um PR de `review/checklist-final` para `main`.
   - Descrever o checklist realizado e pedir revisão final.
6. **Revisão e Mesclagem**:
   - Após aprovação, mesclar o PR na `main`.
   ```bash
   git checkout main
   git merge review/checklist-final
   git push origin main
   ```

### Resumo

1. **Recepção e implementação do feedback do cliente**: Garantir que o layout inicial atende às expectativas do cliente.
2. **Desenvolvimento contínuo e integração de funcionalidades**: Criar feature branches para novas páginas e funcionalidades.
3. **Checklist final**: Revisar todo o código antes do deploy.
