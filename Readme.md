# 🍞 Sistema PDV & Controle de Estoque - Padaria Cheirinho de Pão

## 📝 Resumo do Projeto
Este é um software de **Ponto de Venda (PDV)** e **Gestão de Estoque** desenvolvido sob medida para o segmento de panificação. O sistema foca na agilidade do balcão de atendimento, permitindo a venda de itens por unidade e por peso (balança), com emissão de nota fiscal eletrônica e controle automatizado de entradas e saídas de produtos.

O projeto foi estruturado seguindo o padrão de arquitetura **MVC (Model-View-Controller)** para facilitar a manutenção e garantir a organização entre a interface visual e a lógica de negócios.

---

## 🚀 Tecnologias e Bibliotecas Usadas
* **Linguagem Principal:** Java 21 (LTS).
* **Interface Gráfica:** JavaFX 21 (utilizando FXML para layout e CSS para estilização).
* **Gestão de Dependências:** Maven.
* **Banco de Dados:** PostgreSQL (Persistência de dados de produtos, estoque e vendas).
* **Emissão de NFC-e:** Biblioteca `br.com.swconsultoria` (Comunicação com SEFAZ-SP via WebServices).
* **Relatórios e Impressão:** JasperReports (Geração de DANFE e fechamento de caixa).
* **Códigos de Barras:** Barbecue (Renderização de etiquetas e códigos no DANFE).

---

## 🛠️ Funcionalidades Principais

### Módulo de Vendas
* Leitura de códigos de barras (EAN-13).
* Tratamento de produtos pesáveis com cálculos de precisão decimal (`BigDecimal`).
* Lógica de troco validada conforme regras da SEFAZ (evitando a Rejeição 869).

### Integração Fiscal
* Emissão de NFC-e (modelo 65) em ambiente de **Homologação** e **Produção**.
* Geração de QR Code versão 2.0.
* Tratamento de contingência e erros de validação.

### Gestão de Estoque
* Cadastro de produtos com tributação completa (NCM, CFOP, CEST).
* Atualização automática de saldo após cada venda confirmada.

---

## 📂 Organização das Pastas do Código
A estrutura de pacotes foi organizada para separar as responsabilidades do sistema:

* **conexao**: Gerencia a ponte direta com o banco de dados PostgreSQL.
* **Controller**: Contém a lógica de controle das telas (botões, tabelas e interação com o usuário).
* **entity**: Classes que representam os modelos de dados (Produtos, Vendas, Estoque).
* **enuns**: Armazena as listas de opções fixas e constantes do sistema.
* **repository**: Responsável pela camada de persistência e comandos SQL (DAO).
* **utils**: Ferramentas de apoio, como cálculos de arredondamento e formatadores de moeda.
* **App / Launcher**: Classes responsáveis pela inicialização do sistema e carga do JavaFX.

---

##

<h1>Imagens do Projeto</h1>

<img width="1917" height="1054" alt="painelnicial" src="https://github.com/user-attachments/assets/ab32a789-c280-4cae-b46a-6dfcfb966ffe" />

<img width="1918" height="1054" alt="AtualizarEstoque" src="https://github.com/user-attachments/assets/c9011a06-9a7b-4278-b7a8-109471269d05" />
<img width="1917" height="1053" alt="CadastroProdutos" src="https://github.com/user-attachments/assets/b2705d63-62fc-43dd-9d11-ad50ca13a141" />
<img width="1918" height="1056" alt="CancelarNFE" src="https://github.com/user-attachments/assets/89451bd7-796a-4927-857f-4473a4d128bf" />
<img width="1917" height="1055" alt="PainelVendas" src="https://github.com/user-attachments/assets/110b8d75-06e6-4ffc-abd8-9c44b921e211" />
