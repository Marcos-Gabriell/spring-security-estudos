# Projeto de Estudo: Adicionando Segurança a uma API REST com Spring Security 

## Linguagens e ferramentas  usadas
<div style="display: inline_block">
    <img align="center" alt="java" src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white">
    <img align="center" alt="spring" src="https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white">
    <img align="center" alt="springSecurty" src="https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=Spring-Security&logoColor=white">
    <img align="center" alt="git" src="https://img.shields.io/badge/GIT-E44C30?style=for-the-badge&logo=git&logoColor=white">
    <img align="center" alt="IntelliJ_IDEA" src="https://img.shields.io/badge/IntelliJ_IDEA-000000.svg?style=for-the-badge&logo=intellij-idea&logoColor=white">
</div>


## Resumo

Este projeto de estudo tem como objetivo aprofundar o conhecimento em Spring Security e aplicar práticas avançadas de segurança em aplicações Java usando o ecossistema Spring.

## Introdução

O Spring Security é uma estrutura poderosa e altamente configurável que permite proteger recursos e serviços em aplicativos Spring.Neste projeto, exploraremos essas tecnologias e compreenderemos como integrá-las para criar sistemas de autenticação e autorização robustos.

## Objetivos do Projeto

Os principais objetivos deste projeto de estudo incluem:

1. Aprofundar o entendimento sobre os conceitos fundamentais do Spring Security.
2. Explorar a implementação de autenticação e autorização em aplicativos Spring.
3. Explorar práticas recomendadas de segurança, como proteção contra ataques de segurança comuns.

## Estrutura do Projeto

A estrutura do projeto é a seguinte:

- `src/`: Contém o código-fonte do aplicativo.
- `docs/`: Documentação relacionada ao projeto.
- `exemplos/`: Inclui exemplos de código e configuração.
- `recursos/`: Armazena arquivos e recursos necessários para o projeto.
## Configuração de Segurança

- Configurações de usuário e senha no arquivo `application.properties` para personalizar a autenticação em memória.
- A classe `WebSecurityConfig` estende `WebSecurityConfigurerAdapter` e permite configurar autenticação personalizada em memória. Isso inclui a definição de nomes de usuário, senhas e perfis (roles) para cada usuário.

## Controle de Acesso

- Implementação de endpoints de exemplo em um controlador (`WelcomeController`) que representam diferentes níveis de acesso.
- Uso da anotação `@PreAuthorize` para pré-verificar as permissões de acesso com base nos perfis de usuário.
- Acesso aos recursos é concedido somente se o usuário tiver os perfis (roles) apropriados.

## Pontos Positivos

- Configuração simples e rápida para autenticação em memória.
- Controle flexível de acesso aos recursos com base nos perfis dos usuários.

## Pontos Negativos

- Senhas estáticas e expostas na aplicação, não recomendadas para ambientes de produção.
- Configuração descentralizada com necessidade de adicionar permissões nos controllers.

## Centralização da Configuração

- O método `configure(HttpSecurity http)` na classe `WebSecurityConfig` permite centralizar a configuração de segurança.
- Definição de regras de acesso para diferentes URLs, incluindo acesso público, acesso restrito a perfis específicos e autenticação básica.

## Uso do HTTP Basic Authentication

- O projeto habilita a autenticação básica HTTP para permitir que os clientes enviem suas credenciais sem a necessidade de uma tela de login.
- Isso pode ser útil em APIs onde os clientes precisam autenticar por meio de cabeçalhos de solicitação.

## Referências

- [Documentação oficial do Spring Security](https://docs.spring.io/spring-security/reference/html5/)
- [Documentação oficial do Spring Boot](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/)

## Configuração e Execução

Para executar este projeto em sua máquina local, siga estas etapas:

1. Clone este repositório em sua máquina: `git clone https://github.com/seu-usuario/spring-security-jwt-study`.
2. Navegue até o diretório do projeto: `cd spring-security-jwt-study`.
3. Execute o aplicativo Spring Boot: `./mvnw spring-boot:run`.

Certifique-se de ter o Java e o Maven instalados em sua máquina antes de executar o aplicativo.

## Contribuição

Contribuições são bem-vindas! Se você deseja contribuir para este projeto, siga estas diretrizes:

1. Crie um fork do repositório.
2. Faça suas alterações.
3. Envie um pull request descrevendo suas alterações e os motivos delas.


