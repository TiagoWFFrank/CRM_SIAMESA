Documento de Instalação – RISE CRM (até a etapa atual)
Este documento descreve passo a passo tudo o que foi feito e validado até o momento para instalar o RISE – Ultimate Project Manager & CRM em ambiente local usando XAMPP no Windows.
________________________________________
1. Ambiente utilizado
•	Sistema Operacional: Windows 11
•	Servidor Web: Apache 2.4 (XAMPP)
•	PHP: 8.2.12 (compatível – requisito mínimo do RISE é PHP 8.1)
•	Banco de Dados: MySQL/MariaDB (via phpMyAdmin)
•	Local de instalação: C:\xampp
________________________________________
2. Instalação e configuração do XAMPP
1.	O XAMPP foi instalado fora de Program Files, no caminho:
 	C:\xampp
 	(boa prática para evitar problemas de permissão com UAC).
2.	No XAMPP Control Panel, os serviços abaixo foram iniciados:
o	Apache
o	MySQL
3.	O XAMPP Control Panel foi executado como Administrador.
________________________________________
3. Validação do PHP
A página phpinfo() confirmou:
•	PHP 8.2.12 ativo
•	Arquivo de configuração carregado corretamente:
 	C:\xampp\php\php.ini
Extensões exigidas pelo RISE (todas ativas)
•	mysqli
•	mysqlnd
•	pdo_mysql
•	curl
•	mbstring
•	intl
•	gd
•	dom / xml
•	json
•	zlib (compressão desligada)
Configuração confirmada:
zlib.output_compression = Off
Timezone configurado corretamente:
date.timezone = America/Sao_Paulo
________________________________________
4. Estrutura do projeto
O projeto RISE foi colocado corretamente em:
C:\xampp\htdocs\rise\
Estrutura mínima validada:
rise/
├── app/
├── install/
├── writable/
├── index.php
O instalador está acessível via navegador:
http://localhost/rise/install/
________________________________________
5. Criação do banco de dados
1.	Acesso ao phpMyAdmin:
 	http://localhost/phpmyadmin
2.	Criação do banco de dados:
o	Nome: rise_crm
o	Collation: utf8mb4_general_ci
3.	Situação atual do banco:
o	Banco criado com sucesso
o	Nenhuma tabela criada manualmente (correto, o instalador faz isso)
________________________________________
6. Tela do instalador (status atual)
O instalador do RISE foi acessado com sucesso e encontra-se na etapa:
RISE – Ultimate Project Manager & CRM Installation
Campos apresentados:
6.1 Database connection details
Valores definidos para uso:
•	Database Host: localhost
•	Database User: root
•	Database Password: (vazio)
•	Database Name: rise_crm
•	Table Prefix: rise_
________________________________________
6.2 Administração do sistema
Campos a serem preenchidos pelo administrador:
•	First Name
•	Last Name
•	Email (login)
•	Password
________________________________________
7. Purchase Code (licença)
A licença foi validada via Envato Market / CodeCanyon.
Dados da licença
•	Item: RISE – Ultimate Project Manager & CRM
•	Licença: Regular License
•	Licenciado: ImpulsoCore
•	Autor: FairSketch
Purchase Code utilizado
67ae0233-5b3a-4bd8-9e79-52a371122eab
Este é o único código válido a ser inserido no campo Item purchase code do instalador.
________________________________________
8. Situação atual
Até este ponto:
•	Ambiente validado
•	PHP e extensões corretas
•	Banco criado
•	Estrutura do projeto correta
•	Instalador acessível
•	Purchase Code válido em mãos
🚦 Próximo passo: clicar em Install para concluir a instalação e gerar as tabelas, arquivos de configuração e acesso ao sistema.
APÓS A INSTALAÇÃO EXCLUIR A PASTA INSTALL DO ARQUIVO RISE

rise/install
