# Sistema de Gestão e Emissão de Notas Fiscais
Desenvolvimento colaborativo do site do projeto acadêmico.

## 1. Objetivo e contexto

Este documento reúne as definições principais de planejamento e experiência do usuário para a plataforma de gestão e emissão de Notas Fiscais de Serviço (NFSe). A proposta é centralizar cadastros, emissão e consulta de notas em uma aplicação web responsiva, reduzindo o uso de planilhas e tarefas manuais. O público-alvo são gerentes administrativos, financeiros e proprietários de pequenos negócios.

## 2. Principais dores dos usuários

| Dores identificadas | Necessidades da plataforma |
|---|---|
| Informações espalhadas em planilhas e pastas. | Centralizar notas, cadastros e histórico. |
| Erros no preenchimento manual. | Reutilizar dados cadastrados e validar campos. |
| Dificuldade para localizar notas antigas. | Permitir pesquisa e filtros por número, cliente, data e status. |
| Falta de clareza sobre a situação das notas. | Exibir status de forma simples: autorizada, rejeitada ou pendente. |
| Retrabalho no envio de documentos. | Disponibilizar XML/PDF e opção de envio por e-mail. |
| Dificuldade de uso em dispositivos móveis. | Oferecer interface simples e responsiva. |

## 3. Requisitos principais 

Acesso à plataforma por login, com recuperação de senha e perfis de usuário. Cadastro e consulta de clientes, prestadores, serviços e dados da empresa emitente. Emissão de NFS-e com seleção de cliente e preenchimento dos dados do serviço. Revisão dos dados e indicação de campos obrigatórios ou inconsistências antes do envio. Envio para autorização e apresentação do status retornado pelo serviço. Consulta de notas com pesquisa e filtros por número, cliente, período e status. Visualização dos detalhes e acesso aos arquivos XML/PDF quando disponíveis. Dashboard com resumo das notas, alertas e informações por status.

## 4. Mapa do sistema 

As principais áreas previstas são: Login; Dashboard; Notas Fiscais; Nova Nota Fiscal; Revisão; Resultado do Envio; Detalhes da Nota; Cadastros (clientes, prestadores e serviços); Dados da Empresa; e Usuários e Permissões.

## 5. Fluxo principal do usuário 

1. O usuário realiza o login e acessa o Dashboard. 
2. Seleciona a opção “Nova nota fiscal” e escolhe um cliente cadastrado. 
3. Preenche os dados do serviço e os valores necessários. 
4. Revisa as informações; se houver erro, corrige os campos indicados. 
5. Confirma o envio para autorização. Visualiza o resultado e o status da nota. 
6. Quando disponíveis, consulta os detalhes e baixa os arquivos XML e PDF

## 6. Wireframes e diretrizes de UX/UI

Os wireframes foram desenvolvidos no Figma para representar a estrutura e a organização das principais telas da aplicação, servindo como base para a definição da interface. O projeto considera uma interface simples, intuitiva e responsiva, com padronização dos elementos visuais e facilidade de navegação.

<p align="center">
  <table>
    <tr>
      <td align="center">
        <img src="https://github.com/user-attachments/assets/5b370401-b165-4164-85f9-6d26988117d9" alt="Tela de Login" width="180px"/><br/>
        <sub><b>Login</b></sub>
      </td>
      <td align="center">
        <img src="https://github.com/user-attachments/assets/d45d8aa7-1f93-48e3-be33-363ddf3a6590" alt="Tela de Cadastro" width="180px"/><br/>
        <sub><b>Cadastro</b></sub>
      </td>
      <td align="center">
        <img src="https://github.com/user-attachments/assets/2731b323-bfbf-4fe0-a079-6ee7d109ef43" alt="Tela de Visão Geral" width="180px"/><br/>
        <sub><b>Visão geral</b></sub>
      </td>
    </tr>
    <tr>
      <td align="center">
        <img src="https://github.com/user-attachments/assets/79228559-2549-419d-813d-829677c9cfe0" alt="Tela de Emitir NFS-e" width="180px"/><br/>
        <sub><b>Emitir NFS-e</b></sub>
      </td>
      <td align="center">
        <img src="https://github.com/user-attachments/assets/1f8c642f-f19f-4284-8c5c-6d1422b1fe9c" alt="Tela de Histórico de Notas" width="180px"/><br/>
        <sub><b>Histórico de notas</b></sub>
      </td>
      <td align="center">
        <img src="https://github.com/user-attachments/assets/285d7a3c-1d9f-4cf2-bbfb-1198af33f483" alt="Tela de Configurações" width="180px"/><br/>
        <sub><b>Configurações</b></sub>
      </td>
    </tr>
  </table>
</p>

**Acesso ao wireframes:** [Visualizar no Figma](https://www.figma.com/proto/Z1F2KVItdTjDWApU98bfyq/NF---ADM---PI?node-id=3-15277&t=mKZM1Z97of7UQ5dT-1&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1)

## 7. Protótipo e fluxo de navegação

O protótipo foi desenvolvido no Figma para representar visualmente a aplicação e demonstrar a navegação entre suas principais funcionalidades. O fluxo contempla o acesso à plataforma, o cadastro e a consulta de notas fiscais.

**Acesso ao protótipo:** [Visualizar no Figma](https://www.figma.com/proto/xz5Tmdl1CTy0wQpDpvcKBP/NF---Prot%C3%B3tipo?node-id=3-15277&t=QLNieyNep3wvQmIt-1&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1)

## 8. Tecnologias e ferramentas utilizadas

| Tecnologia/Ferramenta | Utilização |
|---|---|
| Figma | Desenvolvimento dos wireframes e protótipos da aplicação. |
| HTML | Estrutura das páginas de login e cadastro. |
| CSS | Estilização responsiva e componentes visuais compartilhados. |
| JavaScript | Interações simples dos formulários, como mostrar/ocultar senha e validar campos. |

## 9. Estrutura atual do front-end

```text
.
├── assets/
│   ├── css/
│   │   ├── auth.css
│   │   └── dashboard.css
│   ├── js/
│   │   └── auth.js
│   ├── fundo-login.jpg
│   └── logo-nota-facil.png
├── dashboard/
│   └── index.html
├── cadastro/
│   └── index.html
└── login/
    └── index.html
```

Abra `login/index.html`, `cadastro/index.html` ou `dashboard/index.html` em um navegador. Login e cadastro compartilham o mesmo CSS e JavaScript; o painel visual fica diretamente no HTML para manter a implementação simples. A visão geral usa dados estáticos de exemplo. Os formulários e ações precisarão ser conectados a uma API e às demais telas quando o backend for implementado.

## 10. Como rodar o site

Abra o arquivo `index.html` da raiz no navegador. Ele leva para o login, ou para o dashboard se você já estiver logado. A busca automática de CEP funciona melhor servindo a pasta com um servidor local:

```bash
python -m http.server 8000   # depois acesse http://localhost:8000
```

**Conta de demonstração** (já vem com notas de exemplo): `camila@estudioaurora.com.br`, senha `aurora2026`.
Também dá para criar uma conta nova no cadastro. Ela começa sem notas.

## 11. Estrutura de pastas

```
.
├── index.html               entrada: redireciona para login/ ou dashboard/
├── assets/
│   ├── css/
│   │   ├── auth.css         login e cadastro
│   │   ├── dashboard.css    barra lateral, cabeçalho e dashboard (visual de todas as páginas internas)
│   │   └── app.css          formulários, tabelas, modais e nota das páginas internas
│   ├── js/
│   │   ├── auth.js          login, cadastro e sessão
│   │   ├── config.js        endereços das páginas (rotas)
│   │   ├── layout.js        monta menu, cabeçalho, notificações e botão Sair
│   │   ├── store.js         dados salvos no navegador, cálculo do ISS, XML
│   │   ├── utils.js         máscaras, validações, modais, avisos
│   │   ├── icons.js, barcode.js, acoes.js
│   │   └── pages/           um script por página (dashboard, emitir, historico, configuracoes, nota)
│   ├── fundo-login.jpg
│   ├── logo-nota-facil.png
│   └── favicon.svg
├── login/index.html
├── cadastro/index.html
├── dashboard/index.html     Visão geral
├── emitir/index.html        Emitir NFS-e (formulário → envio → resultado)
├── historico/index.html     Histórico: busca, filtros, PDF, editar, cancelar, exportar
├── configuracoes/index.html Dados da empresa, logo, senha, 2 etapas, certificado
└── nota/index.html          Detalhes da nota: PDF, XML e envio por e-mail
```

## 12. Como as páginas se conectam

- Login → `dashboard/`. A sessão fica em `localStorage` (`notafacil:sessao`). Sem sessão, as páginas internas voltam para o login.
- Cadastro → login, com o e-mail já preenchido.
- O menu lateral e o cabeçalho de todas as páginas internas são gerados pelo `assets/js/layout.js`. Para criar uma página nova, copie o esqueleto de uma existente (`<div class="dashboard-layout" data-page="...">` + `<main class="dashboard-content">`) e cadastre o endereço em `assets/js/config.js`.
- O botão **Sair** apaga a sessão e volta para o login.

## 13. Observações

- Os dados ficam salvos no navegador (`localStorage`). Para usar um servidor real, troque as funções de `assets/js/store.js` e `assets/js/auth.js` mantendo os mesmos nomes.
- A autorização da prefeitura é **simulada**, e a tela de resultado informa isso.
- "Salvar PDF" usa a impressão do navegador (destino: Salvar como PDF).

## 14. Limitações e próximos passos

A versão atual da aplicação é uma PoC (Proof of Concept), desenvolvida com foco na validação da interface, navegação e principais funcionalidades do sistema.

A aplicação utiliza JavaScript e Web APIs para implementar recursos de interação, autenticação, gerenciamento de sessão e armazenamento de informações no navegador. A persistência dos dados é realizada por meio da Web Storage API, utilizando o localStorage, permitindo cadastrar, consultar, editar e armazenar informações durante a utilização do sistema.

Essa escolha foi deliberada. Como a disciplina é EAD e não há data definida para a avaliação, um servidor externo gratuito poderia estar suspenso por inatividade no momento da correção. Manter o backend no navegador e publicar a aplicação no GitHub Pages garante **disponibilidade permanente e custo zero**, sem depender de serviço externo.

Optamos por entregar um **backend simulado no cliente**. Toda a lógica de negócio (cálculo de ISS, geração de chave de acesso, controle de status, histórico de eventos, regras de edição e cancelamento) e o repositório de dados foram implementados em JavaScript, com persistência via localStorage. Dessa forma, a PoC demonstra a construção da lógica e a integração dos dados de ponta a ponta, mesmo sem um servidor clássico.
Como as páginas só consomem as funções desses módulos, a migração para um servidor real exige apenas substituí-las por chamadas a uma API, mantendo os mesmos nomes, sem alterar a interface.

**Funcionamento e escopo da PoC.** Todas as funcionalidades previstas no escopo da PoC estão implementadas e foram demonstradas em funcionamento no vídeo, incluindo cadastro, login, emissão, consulta e gerenciamento de notas fiscais. Cada funcionalidade possui lógica de negócio própria e opera sobre um modelo de dados definido, com entidades (usuário, empresa emitente, cliente, serviço e nota fiscal) e relacionamentos entre elas. O que é simulado é a infraestrutura: o navegador do usuário assume o papel do servidor, executando a lógica e armazenando os dados localmente via localStorage. Por isso, os dados persistem no navegador em que foram criados.

**Organização da camada de dados.** O localStorage é apenas o mecanismo de armazenamento. A organização dos dados é feita por entidades, com relacionamentos entre elas (por exemplo, uma nota fiscal está associada a um cliente e à empresa emitente). O acesso a essas entidades fica concentrado em módulos de repositório (`assets/js/store.js` e `assets/js/auth.js`), separados das telas (`assets/js/pages/`), o que mantém as regras de negócio isoladas da interface.

São utilizadas também integrações com serviços externos, como a API ViaCEP, para automatizar a consulta de endereços a partir do CEP informado pelo usuário.

A autorização das notas fiscais pela prefeitura é simulada nesta versão, permitindo demonstrar o fluxo de emissão e acompanhamento dos status das NFS-e.

Hospedagem da aplicação. O projeto está publicado no GitHub Pages, que atua como servidor externo de hospedagem estática, disponibilizando a aplicação pela internet por meio de um navegador, sem necessidade de instalação local. A lógica de negócio e a persistência dos dados continuam sendo executadas no navegador do usuário. Link: https://eddcarrilho.github.io/Project-NF-S/

Como evolução do projeto, estão previstas melhorias na infraestrutura de armazenamento, integração com serviços externos de autorização fiscal e expansão dos recursos de gerenciamento e segurança dos dados.


## 15. Vídeo de Demonstração 

[Assistir ao vídeo de demonstração da aplicação](https://youtu.be/VB7mLsBXKKU)

_Vídeo realizado por Leticia Vanni De Aquino._

## 16. Integrantes

* Eduardo Sewnarine Carrilho
* Jhulia Mirelli Tomasi
* Kayk Junior Da Silva Trindade
* Kevillyn Sandes Dos Santos
* Leticia Vanni De Aquino
* Luan Castilho Batista Da Silva
