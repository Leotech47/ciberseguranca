# Phishing para captura de senhas do Facebook

### Ferramentas

- Kali Linux
- setoolkit

### Configurando o Phishing no Kali Linux

- Acesso root: ``` sudo su ```
- Iniciando o setoolkit: ``` setoolkit ```
- Tipo de ataque: ``` Social-Engineering Attacks ```
- Vetor de ataque: ``` Web Site Attack Vectors ```
- Método de ataque: ```Credential Harvester Attack Method ```
- Método de ataque: ``` Site Cloner ```
- Obtendo o endereço da máquina: ``` ifconfig ```
- URL para clone: http://www.facebook.com

### Resutados

![Alt text](./passwd.png "Optional title")

O ataque descrito no link se refere a um **ataque de phishing**, uma técnica de **engenharia social** onde um atacante tenta enganar a vítima para que ela revele informações confidenciais, como senhas, dados bancários ou informações pessoais, através de um site falso ou um e-mail fraudulentamente enviado. Vou te explicar detalhadamente como esse ataque funciona e os conceitos envolvidos.

---

### **1. O que é Phishing?**

O **phishing** é uma das formas mais comuns de ataque em cibersegurança, em que o atacante tenta enganar a vítima para que ela forneça informações sensíveis, como senhas, números de cartões de crédito ou dados bancários. O termo "phishing" vem da ideia de "pescar" as informações da vítima, como se fossem peixes.

O atacante geralmente usa uma técnica de **engenharia social**, em que ele tenta se passar por uma entidade confiável (um banco, empresa de tecnologia ou um amigo), para induzir a vítima a realizar alguma ação, como clicar em um link malicioso ou baixar um arquivo infectado.

---

### **2. Como Funciona um Ataque de Phishing?**

#### **Passo 1: Preparação do Ataque**
Para iniciar um ataque de phishing, o atacante geralmente segue estas etapas:

- **Escolher um alvo**: Pode ser uma pessoa específica, uma organização ou um grupo de usuários.
- **Criação do site falso**: O atacante cria um site falso, que parece legítimo. Este site pode ser uma cópia exata de um banco, rede social ou qualquer outro serviço que a vítima use.
- **Envio de um e-mail de phishing**: O atacante envia um e-mail para a vítima, geralmente fazendo com que pareça uma comunicação legítima. O e-mail pode parecer vir de um banco, serviço de email ou qualquer outra entidade confiável. Esse e-mail geralmente solicita que a vítima clique em um link para "atualizar sua senha", "confirmar uma transação" ou "verificar sua conta". O link leva a uma página falsa.
  
O atacante pode usar ferramentas como **kits de phishing**, que permitem criar sites de phishing de maneira rápida e automatizada.

#### **Passo 2: Indução da vítima**
O e-mail enviado para a vítima normalmente terá uma mensagem que tenta pressioná-la a agir rapidamente. Por exemplo:
- "Sua conta foi acessada por um dispositivo não autorizado, clique aqui para verificar."
- "Seu acesso foi bloqueado, clique aqui para restaurar sua conta."
  
Esses tipos de mensagens geram um senso de urgência e medo, o que pode levar a vítima a clicar no link sem pensar nas consequências.

#### **Passo 3: Coleta de dados sensíveis**
Ao clicar no link do e-mail de phishing, a vítima é redirecionada para um site falso, que parece ser o site verdadeiro. Ao inserir suas credenciais (como nome de usuário e senha), essas informações são enviadas diretamente para o atacante.

O atacante, agora com as credenciais da vítima, pode acessar contas bancárias, redes sociais, e-mails, e outros serviços importantes, dependendo do tipo de informações que foram fornecidas.

#### **Passo 4: Uso das informações obtidas**
Uma vez que o atacante tem as informações necessárias, ele pode:
- Acessar a conta da vítima e roubar dinheiro ou dados pessoais.
- Usar as credenciais para fazer transações fraudulentas ou obter outros dados sensíveis.
- Espalhar o ataque para outras vítimas, como amigos ou familiares da vítima, se ela usar as mesmas credenciais em outros sites.

---

### **3. Como os Ataques de Phishing São Planejados?**

No contexto do **GitHub** que você mencionou, o repositório fala sobre **desafios de phishing**, o que geralmente se refere a **exercícios práticos para identificar e proteger-se contra ataques de phishing**. O repositório provavelmente descreve como os atacantes podem criar um site de phishing e como defender-se desse tipo de ataque. A sequência típica de planejamento de um ataque de phishing envolve:

1. **Escolha do alvo**: Identificar as vítimas potenciais.
2. **Criação do site de phishing**: Isso envolve clonar um site legítimo ou criar um site falso com o mesmo visual. O atacante pode usar ferramentas como **Social-Engineer Toolkit (SET)** para gerar páginas de login falsas.
3. **Disfarce do link de phishing**: O atacante cria links curtos ou parece usar um link legítimo (por exemplo, um link que redireciona para o site falso). Isso pode ser feito com o uso de **encurtadores de URL** ou manipulando o nome do domínio para parecer confiável.
4. **Envio do link para a vítima**: Através de e-mails, mensagens de texto ou até redes sociais.

O atacante tem como objetivo capturar as credenciais da vítima de forma a invadir suas contas.

---

### **4. Como Defender-se de Phishing?**

Aqui estão algumas medidas para se proteger contra ataques de phishing:

- **Verificação de URLs**: Sempre verifique a URL do site para ter certeza de que está no site correto. Sites de phishing muitas vezes utilizam domínios falsos, como "www.banco-brasil.com" ao invés de "www.bancobrasil.com.br".
  
- **Uso de autenticação multifator (MFA)**: Mesmo que um atacante obtenha suas credenciais, se você tiver **autenticação multifator** ativada, o atacante não conseguirá acessar sua conta sem o segundo fator.

- **Desconfiança em links suspeitos**: Nunca clique em links de e-mails ou mensagens de fontes desconhecidas. Sempre acesse os sites diretamente digitando o endereço na barra de navegação.

- **Educação e treinamento**: O fator humano é um dos maiores pontos fracos na segurança cibernética. Empresas devem treinar seus funcionários para reconhecer sinais de phishing e como evitá-los.

- **Ferramentas de segurança**: Utilize ferramentas como filtros de spam, antivírus e **anti-phishing** para bloquear e-mails e sites fraudulentos.

---

### **5. Exemplos de Ferramentas Usadas em Ataques de Phishing**

- **Social-Engineer Toolkit (SET)**: Uma ferramenta popular usada para criar e-mails de phishing e páginas de login falsas.
- **Kits de Phishing**: Pacotes de software prontos para uso que podem automatizar a criação de sites de phishing, como **Evilginx** (para ataques de phishing em duas etapas) ou **Gophish** (ferramenta de phishing de código aberto).
- **E-mail Spoofing**: Técnicas para falsificar o endereço do remetente e fazer o e-mail parecer que vem de uma fonte confiável.

---

### **Conclusão**

O ataque de phishing é uma ameaça muito comum e eficaz devido à sua capacidade de manipular a psicologia humana. O atacante explora a confiança da vítima, muitas vezes em nome de empresas ou serviços que ela já conhece. A chave para se proteger contra esse tipo de ataque é o **treinamento contínuo**, a **verificação cuidadosa** dos links e **ferramentas de segurança adequadas**.  

Ao aprender sobre como os ataques de phishing funcionam e como prevenir e detectar tais ataques, você está tomando as medidas necessárias para se proteger e proteger os outros contra esse tipo de ameaça.

