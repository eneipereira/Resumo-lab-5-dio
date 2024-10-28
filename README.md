# Resumo-lab-5-dio

## Introdução

O Azure oferece várias opções de armazenamento, adequadas para diferentes tipos de dados e necessidades, como arquivos, discos, tabelas, e filas. O Azure Storage é amplamente utilizado por aplicativos em nuvem para armazenar dados não estruturados, dados de backup, logs, e muito mais.

## Principais Tipos de Armazenamento no Azure:

### 1. Blob Storage (Objetos de Blob):

Uso: Ideal para armazenar grandes quantidades de dados não estruturados, como imagens, vídeos, backups, logs ou arquivos de qualquer tipo.

Categorias:

Blobs de Bloco: Para armazenar dados de upload em blocos, como arquivos de mídia ou documentos.

Blobs de Página: Para armazenar arquivos usados para VMs (discos virtuais, por exemplo).

Blobs de Anexos: Para modificar blocos individuais dentro de um arquivo grande.


Níveis de Acesso: O Blob Storage oferece níveis de acesso baseados na frequência com que os dados são acessados:

Hot: Para dados acessados frequentemente.

Cool: Para dados acessados menos frequentemente, mas que precisam de disponibilidade.

Archive: Para dados raramente acessados, com alta latência de recuperação.

### 2. Azure Files:

Uso: Oferece compartilhamento de arquivos SMB (Server Message Block) e NFS (Network File System) na nuvem, ideal para aplicações legadas que precisam acessar sistemas de arquivos compartilhados.

Vantagem: Pode ser montado diretamente em máquinas virtuais (VMs) ou em servidores locais, permitindo fácil integração entre ambientes on-premises e na nuvem.

### 3. Disk Storage:

Uso: Armazenamento de discos gerenciados para Máquinas Virtuais (VMs). Os discos podem ser SSDs (Solid State Drives) ou HDDs (Hard Disk Drives), dependendo da performance e do custo.

Tipos:

Premium SSD: Para VMs de alto desempenho com workloads intensivas em I/O.

Standard SSD: Uma opção de baixo custo para workloads menos intensivas.

Standard HDD: Armazenamento econômico para dados de acesso esporádico.

### 4. Table Storage:

Uso: Um banco de dados NoSQL para armazenar grandes quantidades de dados estruturados de forma chave-valor. É ideal para cenários onde grandes quantidades de dados precisam ser armazenados e acessados rapidamente.

Características: Oferece armazenamento simples e escalável, usado para dados como logs, configurações, ou dados de aplicativos.

### 5. Queue Storage:

Uso: Serviço de mensagens assíncronas usado para comunicação entre componentes de um sistema distribuído. As filas do Azure são ideais para orquestrar o processamento em segundo plano ou para equilibrar a carga de tarefas.

## Passo a Passo para Criar um Armazenamento no Azure:

### 1. Acessar o Portal do Azure:

Entre no Portal do Azure.

### 2. Criar uma Conta de Armazenamento:

No menu do portal, clique em Contas de Armazenamento e selecione Criar.

Escolha a Assinatura correta e o Grupo de Recursos onde deseja colocar a conta de armazenamento.

Defina o Nome da conta (único e globalmente acessível).

Selecione a Região onde os dados serão armazenados.

Escolha o tipo de Desempenho:

Standard: Armazenamento econômico com HDDs para dados de acesso esporádico.

Premium: Armazenamento baseado em SSDs para aplicações de alta performance.


Escolha a Redundância:

Locally Redundant Storage (LRS): Mantém cópias dos dados dentro da mesma região.

Geo-Redundant Storage (GRS): Mantém cópias dos dados em outra região geograficamente distante para maior segurança.

### 3. Configurar Opções Avançadas (opcional):

Configure Criptografia se precisar de opções personalizadas.

Defina as Configurações de Rede para limitar ou permitir o acesso à conta de armazenamento de endereços IP específicos ou redes virtuais.

### 4. Revisar e Criar:

Após definir as configurações, clique em Revisar + Criar e, em seguida, Criar.

### 5. Usar o Armazenamento:

Após a criação da conta, você pode acessar os diversos tipos de armazenamento (Blob, Files, Tables, Queues) através do portal, SDKs do Azure, ou ferramentas como Azure Storage Explorer.

### Exemplos de Uso:

Backup e Arquivamento: Usar o Blob Storage para backups de arquivos, sistemas e logs, com opção de mover dados para o nível Archive quando não são mais frequentemente acessados.

Hospedagem de Aplicações Web: Usar Azure Files para compartilhar arquivos entre diferentes VMs ou servidores locais e nuvem.

Discos de VMs: Adicionar Disk Storage a VMs para armazenar dados de aplicação com alta confiabilidade e desempenho.

Processamento em Lote: Usar Queue Storage para gerenciar tarefas e processá-las de forma assíncrona, otimizando o fluxo de trabalho.
