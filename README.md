<!DOCTYPE html>
<html>
<head>
  <title>README - Configuração do Terraform para instância do AWS EC2</title>
</head>
<body>
  <h1>README - Configuração do Terraform para instância do AWS EC2</h1>

  <p>Este repositório contém um código em Terraform para criar uma instância do Amazon EC2 na região "us-west-2" usando o provedor AWS. O objetivo deste código é fornecer uma estrutura inicial para criar e gerenciar recursos da AWS de forma programática.</p>

  <h2>Requisitos</h2>

  <p>Antes de executar este código, verifique se você possui os seguintes requisitos:</p>

  <ol>
    <li>Terraform instalado (versão mínima 1.2.0)</li>
    <li>Credenciais de acesso da AWS configuradas no seu ambiente local</li>
    <li>Chave SSH existente para se conectar à instância EC2</li>
  </ol>

  <h2>Configuração</h2>

  <ol>
    <li>Clone este repositório para o seu ambiente local.</li>
    <li>Certifique-se de ter as credenciais corretas da AWS configuradas. Isso pode ser feito definindo variáveis de ambiente ou usando perfis de configuração. O perfil "default" será usado neste exemplo.</li>
    <li>Verifique se você tem uma chave SSH existente para se conectar à instância EC2. A chave "iac-primer" será usada neste exemplo. Caso você não tenha uma chave SSH, você precisará criar uma antes de prosseguir.</li>
    <li>Abra o arquivo <code>main.tf</code> e revise as configurações. Neste exemplo, uma instância do tipo "t2.micro" será criada usando a imagem AMI "ami-03f65b8614a860c29" da região "us-west-2". Você pode modificar essas configurações de acordo com suas necessidades.</li>
    <li>Execute o comando <code>terraform init</code> para inicializar o projeto do Terraform. Isso garantirá que os plugins e provedores necessários sejam baixados e instalados.</li>
    <li>Em seguida, execute o comando <code>terraform apply</code> para criar a instância EC2. O Terraform solicitará sua confirmação antes de realizar qualquer alteração na sua infraestrutura.</li>
    <li>Após a confirmação, o Terraform criará a instância EC2 e atribuirá as tags especificadas no arquivo <code>main.tf</code>. Essas tags são úteis para identificar e organizar recursos na AWS.</li>
    <li>Você pode acessar a instância EC2 usando a chave SSH configurada anteriormente e o endereço IP público fornecido pelo Terraform após a conclusão da implantação.</li>
  </ol>

  <h2>Limpeza</h2>

  <p>Para evitar custos desnecessários, é recomendado que você destrua os recursos criados após usá-los. Para fazer isso, execute o comando <code>terraform destroy</code>. O Terraform solicitará sua confirmação antes de remover os recursos.</p>

  <h2>Conclusão</h2>

  <p>Este código em Terraform fornece uma estrutura básica para criar uma instância EC2 na AWS usando a linguagem de infraestrutura como código. Você pode usar isso como ponto de partida para criar infraestruturas mais complexas e automatizadas na AWS.</p>

  <p><strong>Observação:</strong> Lembre-se de sempre revisar e adaptar as configurações de acordo com suas necessidades específicas antes de implantar qualquer infraestrutura usando o Terraform.</p>
</body>
</html>
