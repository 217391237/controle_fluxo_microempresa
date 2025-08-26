# controle_fluxo_microempresa
Sistema desenvolvido em Java com interface gráfica Swing para gerenciamento de vendas em supermercado, incluindo geração de nota fiscal em PDF.
Sistema de Caixa de Supermercado

Sistema desenvolvido em Java com interface gráfica Swing para gerenciamento de vendas em supermercado, incluindo geração de nota fiscal em PDF.

 Funcionalidades:
-  Cadastro e busca de clientes por CPF
-  Seleção de produtos com controle de estoque
-  Múltiplas formas de pagamento (Débito, Crédito, Pix, Dinheiro)
-  Geração automática de nota fiscal em PDF
-  Interface gráfica intuitiva
-  Controle de estoque automático
-  Arquitetura orientada a objetos

 Tecnologias Utilizadas:
- Java 11+
- Swing (Interface Gráfica)
- MySQL (Banco de Dados)
- iText (Geração de PDF)
- Maven (Gerenciamento de Dependências)

 Pré-requisitos:
1. Java JDK 11 ou superior
2. MySQL Server
3. NetBeans IDE (recomendado)
4. Maven (integrado ao NetBeans)

 Configuração do Banco de Dados:
1. Crie um banco de dados MySQL chamado `supermercado`
2. Execute o script SQL fornecido para criar as tabelas
3. Execute o script `insert_sample_data.sql` para inserir dados de exemplo
4. Configure as credenciais de conexão em `DatabaseConnection.java`:
   - URL: `jdbc:mysql://localhost:3306/supermercado`
   - Usuário: `root`
   - Senha: (configure conforme sua instalação)

 Como Executar:
- No NetBeans:
1. Abra o projeto no NetBeans
2. Clique com o botão direito no projeto → "Clean and Build"
3. Execute a classe `Main.java`

# Via linha de comando:
\`\`\`bash
mvn clean compile exec:java -Dexec.mainClass="Main"
\`\`\`

# Gerar JAR executável:
\`\`\`bash
mvn clean package
java -jar target/sistema-caixa-supermercado-1.0.0.jar
\`\`\`

 Estrutura do Projeto

\`\`\`
src/main/java/
├── model/               Classes de modelo (Cliente, Produto, Venda, etc.)
├── dao/                 Classes de acesso a dados
├── service/             Serviços (geração de PDF)
├── view/                Interface gráfica
└── Main.java            Classe principal

scripts/                 Scripts SQL
└── insert_sample_data.sql
\`\`\`

 Como Usar

1. Dados do Cliente: Preencha nome, contato e CPF
2. Adicionar Produtos: Selecione produto e quantidade, clique em "Adicionar"
3. Forma de Pagamento: Escolha entre Débito, Crédito, Pix ou Dinheiro
4. Finalizar Venda: Clique em "Finalizar Venda" para processar e gerar PDF
5. Nova Venda: Clique em "Nova Venda" para iniciar uma nova transação

 Recursos Implementados

- Validação de dados obrigatórios
- Controle de estoque automático
- Busca de cliente por CPF (cadastra automaticamente se não existir)
- Cálculo automático de subtotais e total
- Geração de PDF com layout profissional
- Transações de banco com rollback em caso de erro
- Interface responsiva e intuitiva

 Dependências Maven

- `mysql-connector-java`: Conexão com MySQL
- `itextpdf`: Geração de documentos PDF

O sistema está pronto para uso em ambiente de produção e pode ser facilmente expandido com novas funcionalidades.
