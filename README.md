# QR Code Generator com Java Spring Boot
Este projeto permite gerar QR Codes dinâmicos e armazená-los automaticamente em um bucket do Amazon S3, utilizando o framework Spring Boot e a biblioteca ZXing.
- Criado baseado em: https://www.youtube.com/watch?v=71WGVa79BWE (Fernanda Kipper)
## 🚀 Tecnologias Utilizadas
Backend:
Java 11+
Spring Boot
ZXing (Zebra Crossing)
Amazon S3

## 🧠 Funcionalidades
- Geração de QR Codes dinâmicos a partir de dados fornecidos pelo usuário.
- Armazenamento automático dos QR Codes gerados em um bucket do Amazon S3.
- Acesso público aos QR Codes gerados via URL fornecida pelo S3.

## ⚙️ Como Executar o Projeto
1. Clonar o repositório
```bash
git clone https://github.com/Caduzinhok/qrcode-generator.git
```
2. Configurar as credenciais do AWS S3
Crie um arquivo .env e com as seguintes configurações:
```bash
aws.accessKeyId=SEU_ACCESS_KEY
aws.secretKey=SEU_SECRET_KEY
```
3. Executar o projeto
No diretório raiz do projeto, execute:

```bash
O servidor estará disponível em http://localhost:8080.
```

4. Gerar um QR Code
- Acesse a URL: http://localhost:8080/qrcode
- Passe como parâmetro um json:
```bash
{
  "text":"seu_link_aqui"
}
```

- O QR Code gerado será armazenado no bucket S3 e você receberá a URL pública para acessá-lo.

## 📁 Estrutura do Projeto
```bash
qrcode-generator/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── caduzinhok/
│   │   │           └── qrcodegenerator/
│   │   │               ├── controller/
│   │   │               ├── service/
│   │   │               └── util/
│   │   └── resources/
│   │       └── application.properties
├── pom.xml
└── README.md
```
## 📌 Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull request
