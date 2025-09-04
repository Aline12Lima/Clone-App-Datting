# Observações do Projeto Instalações
Este arquivo dedico a quem deseja praticar essas ferramentas e aprender novas formas de resolver problemas, se atualizar e desenvolver o conhecimento. 

## Ferramentas
Este projeto tem como objetivo praticar as seguintes ferramentas
Next.js
Tailwind.css
React.js
Supabase
Stream 
Git
VsCode
Ubuntu
typeScript

## comandos
npx create-next-app
este comando cria as dependências necessárias pelo next.js
Exemplo: 

nome-do-projeto/
 ┣ node_modules/
 ┣ public/
 ┣ src/ (se você escolher essa opção)
 ┣ app/ ou pages/ (depende da versão e do setup que escolher)
 ┣ .gitignore
 ┣ next.config.mjs   ✅
 ┣ package.json
 ┣ tsconfig.json (se escolher TypeScript)
 ┣ README.md

É importante selecionar as opções no terminal quando roda o npx,
porque vocÊ vai informar nome do projeto, se vai usar tailwind, typeScript....
Diante de cada dúvida ou palavras novas é importante pausar e entender. 
Quando estamos aprendendo não se trata de corrida contra o tempo e sim conhecer algo novo respeitando seu ritmo de aprendizado. 
## Back-end
O Supabase
O Supabase é uma plataforma de backend como serviço (BaaS) que fornece funcionalidades semelhantes ao Firebase, mas com foco em open-source e PostgreSQL. Ele facilita a criação de aplicações web e móveis sem precisar gerenciar manualmente servidores ou bancos de dados complexos.

A pasta LIB guarda a integração da supabese entre cliente e servidor, o npm install supabase no terminal é necessário, o doc .env.local guarda informações da API,  faça login e siga as orientações para usa-lo corretamente. 


## Rotas
é necessário saber como funciona o next.js, antes de iniciar o projeto. 
ESpero que já tenha estudado react e feito algum projeto para entender como ele funciona.  As rotas é fundamental. 

# Hooks
Por padrão no next.js, por padrão os componentes do app Router são Server componentes, eles rodam no servidor e nao pode usar hooks, isso porque carregam dados direto do banco e renderiza Html estatico/SSR..
Mas e se vcoê precisa de Hooks?
como o useState? useEffect, useContext..... eventos como Onclick,onChange?
É Só tranformar o componente em client component usando o "use client" no inicio da pagina. 

# APP page [app/page.tsx](../app/page.tsx) - Página inicial 
Dentro desta página criaamos a autenticação que é login com input para email e senha. botão com onClick. e nele temos um codigo interessante que é aquele texto em forma de link, que pergunta se vocÊ tem conta então informe email e senha se nao tem conta cadastre. 

 {isSignUp
              ? "Already have an account? Sign in"
              : "Don't have an account? Sign up"}

# form
No formulário da página App auth, foi usado o  onSubmit={handleAuth},essa função serve para  direcionar o usuário para as rotas necessárias por exemplo tratativas iniciais:  
setLoading(true);
setError("") .
Se os dados informados for true vai pararecer loading. Se não error.
try e catch pega o erro e trata

# use um email valido para testar, se você informar um email valido ele precisa aparece na plataforma do supabase em autenticações e vocÊ receberá um email de confirmação. olhe o consele.log também. 

# contexts (../context.page.tsx)