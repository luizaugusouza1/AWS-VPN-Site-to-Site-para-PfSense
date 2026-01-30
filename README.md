# 🌐 AWS VPN Site-to-Site com pfSense

Este projeto demonstra a **implementação prática de uma VPN Site-to-Site entre um ambiente on-premises utilizando pfSense e uma VPC privada na AWS**.  
O objetivo é permitir **comunicação segura entre redes locais e sub-redes privadas na AWS**, sem expor recursos à internet pública.

📌 Projeto desenvolvido com foco **educacional e prático**, simulando um cenário real de infraestrutura corporativa.

---

## 🧠 Visão Geral da Arquitetura

A solução utiliza os seguintes componentes:

- **pfSense** como firewall e gateway VPN (on-premises)
- **AWS Site-to-Site VPN**
- **Customer Gateway**
- **Virtual Private Gateway (VGW)**
- **VPC com sub-redes privadas**
- **Instâncias EC2 em subnet privada**
- **Criptografia IPsec (IKEv1 / ESP)**

A VPN foi configurada em **modo Route-Based**, garantindo maior flexibilidade de roteamento.

---

## 🖼️ Imagens do Projeto

### 🔐 VPN AWS Site-to-Site + pfSense
![AWS VPN Site to Site](images/imagem1.jpg)

---

### 📊 Status do IPsec no pfSense
Conexão estabelecida com **duas fases (Phase 1 e Phase 2)** ativas e tráfego fluindo corretamente.
![pfSense IPsec Status](images/imagem2.png)

---

### ☁️ AWS – Virtual Private Gateway e VPN
Visualização da VPN ativa no console da AWS.
![AWS VPN Gateway](images/imagem3.png)

---

### 🗺️ Diagrama da Arquitetura
Fluxo completo da comunicação entre rede local e AWS VPC privada.
![Arquitetura AWS VPN](images/imagem4.png)

---

## 🔧 Configurações Técnicas (Resumo)

### 🔑 IPsec
- **Tipo:** Site-to-Site
- **Modo:** Route-Based
- **IKE:** v1
- **Criptografia:** AES-128
- **Autenticação:** SHA1
- **PFS:** Enabled
- **Túneis:** 2 (Alta disponibilidade)

### 🌐 Redes
- **Rede local (On-premises):** `10.0.1.0/24`
- **Rede remota (AWS VPC):** `200.0.0.0/24`

---

## ✅ Testes Realizados

✔️ Ping da máquina local para EC2 na subnet privada  
✔️ Ping da EC2 para gateway local
✔️ Acessar remotamente o EC2 com SSH  
✔️ Comunicação bidirecional validada  
✔️ VPN estável com tráfego contabilizado no IPsec  

---

## 🎥 Vídeo Explicativo no YouTube

📺 Assista ao vídeo completo com a explicação passo a passo da configuração:

👉 https://www.youtube.com/watch?v=gBGADjKhYHc

---

## 🔗 Links Importantes

- 💼 **LinkedIn**  
  https://www.linkedin.com/in/luiz-inhesta-341b4b311/

- 📺 **Canal no YouTube**  
  https://www.youtube.com/@luizinhesa

---

## 🚀 Objetivo do Projeto

Este laboratório tem como objetivo:

- Demonstrar **integração real entre on-premises e AWS**
- Aplicar conceitos de **segurança, redes e cloud**
- Servir como **material de estudo e portfólio profissional**
- Auxiliar profissionais iniciantes e intermediários em **VPN na AWS**

---

## 📌 Observações

🔒 Este projeto utiliza **boas práticas de segurança**, porém deve ser adaptado conforme o ambiente de produção.  
📚 Ideal para estudos de **Cloud, Redes, Segurança e Infraestrutura**.

---

## ✍️ Autor

**Luiz Inhesta**  
Especialista em Infraestrutura, Redes e Cloud ☁️🔥  

Se este projeto te ajudou, deixe uma ⭐ no repositório!
