# Aparatus - Sistema de Agendamento Fullstack

Aparatus é uma plataforma moderna de agendamento de serviços (Barbearias). O foco do projeto foi construir uma aplicação escalável, com experiência de usuário fluida e integração de pagamentos reais.

Link: https://aparatus-woad.vercel.app/

## Sobre o Projeto

O Aparatus resolve o problema de agendamentos manuais, permitindo que clientes visualizem horários disponíveis em tempo real, realizem reservas e efetuem o pagamento via cartão de crédito ou Pix, tudo em uma única interface.

### Principais Funcionalidades:
- **Autenticação Segura:** Login social via Google utilizando NextAuth.
- **Reserva de Horários:** Sistema inteligente que impede agendamentos duplicados.
- **Gestão de Pagamentos:** Integração com Stripe para checkout e reembolsos automáticos.
- **Interface Responsiva:** Design otimizado para Mobile e Desktop com Shadcn/UI.
- **Confirmação via Chat:** Integração de IA para auxílio no fluxo de agendamento.

## Tecnologias Utilizadas

### Front-end
- **Next.js 15 (App Router)**: Framework React para performance e SEO.
- **Tailwind CSS**: Estilização baseada em utilitários.
- **Shadcn/UI**: Componentes de interface de alta qualidade.
- **Lucide React**: Biblioteca de ícones.

### Back-end & Banco de Dados
- **Prisma ORM**: Modelagem de dados e comunicação com o banco.
- **PostgreSQL**: Banco de dados relacional para alta integridade.
- **NextAuth.js**: Fluxo de autenticação e proteção de rotas.
- **Stripe API**: Processamento seguro de pagamentos.

### DevOps & Ferramentas
- **Docker**: Containerização do banco de dados para ambiente de dev.
- **Vercel**: Deploy automatizado e hospedagem.
- **Zod**: Validação de esquemas e tipos.

## Como Executar o Projeto

1. **Clone/baixe o repositório:**
    Link

2. **Instale as dependências:**
    No terminal: pnpm install

3. **Configure o banco de dados:**
    Crie um banco de dados no pgadmin

4. **Configure as variáveis de ambiente:**
    Renomeie o .env.example para .env e coloque as informações do seu banco de dados, como usuário e senha, seguindo o modelo: DATABASE_URL="postgresql://seu_usuario:sua_senha@localhost:5432/nome_do_banco"

5. **Rode as migrações do Prisma:**
    No terminal: npx prisma migrate dev

6. **Popule o banco de dado:**
    No terminal: npx prisma db seed

7. **Pronto! Agora é so rodar a aplicação com:**
    No terminal: pnpm dev

8. **Prisma Studio(OPCIONAL):**
    No terminal: npx prisma studio
    - Abre uma interface web fácil para editar tabelas e substituir nomes, serviços, usuários etc.
    OBS: Se você preferir editar diretamente no banco, dá para atualizar qualquer tabela manualmente, no pgAdmin.

# Diferenciais Técnicos

Neste projeto, apliquei conceitos avançados de desenvolvimento:

- Server Components & Server Actions: Redução de JavaScript no lado do cliente e segurança nas transações.

- Webhooks do Stripe: Implementação de lógica assíncrona para confirmar pagamentos e disparar ações no banco de dados.

- Tipagem Estrita: Uso de TypeScript em todo o projeto para evitar erros em tempo de execução.

- UI/UX: Foco em estados de carregamento (skeletons) e feedback visual imediato para o usuário.