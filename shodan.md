### **Shodan: A Ferramenta de Busca para Dispositivos Conectados à Internet**

#### **O que é o Shodan?**
Shodan é um motor de busca especializado que permite encontrar dispositivos conectados à internet, como servidores, roteadores, câmeras de segurança, sistemas industriais (ICS/SCADA), dispositivos IoT (Internet das Coisas) e muito mais. Diferente do Google, que indexa páginas da web, o Shodan varre a internet em busca de informações sobre dispositivos e seus serviços.

Foi criado por **John Matherly** em 2009 e se tornou uma ferramenta essencial para profissionais de segurança cibernética, administradores de redes e pesquisadores de segurança, pois permite identificar vulnerabilidades e monitorar a exposição de dispositivos críticos.

---

### **Como o Shodan Funciona?**
O Shodan realiza buscas por dispositivos conectados à internet coletando **banners** — informações que os dispositivos expõem quando estão acessíveis. Os banners podem conter detalhes como:

- Endereço IP
- Tipo de dispositivo
- Protocolo em uso (HTTP, FTP, SSH, Telnet, RDP, etc.)
- Versões de software/firmware
- Nome do fabricante
- Localização geográfica
- Certificados SSL/TLS
- Configurações de segurança

O Shodan utiliza scanners distribuídos globalmente para mapear a internet constantemente e atualizar seu banco de dados.

---

### **Principais Aplicações do Shodan**
O Shodan tem diversos usos, tanto legítimos quanto potencialmente perigosos, dependendo da intenção do usuário.

#### **1. Segurança Cibernética e Testes de Intrusão**
- Identificação de dispositivos vulneráveis.
- Busca por servidores ou roteadores mal configurados.
- Descoberta de portas abertas e serviços expostos.
- Monitoramento de sistemas críticos para evitar invasões.

#### **2. Pesquisa e Inteligência de Ameaças**
- Identificação de novas ameaças e tendências no cenário cibernético.
- Análise de vulnerabilidades em sistemas IoT e industriais.
- Coleta de informações para estudos acadêmicos e investigações.

#### **3. Monitoramento de Infraestruturas Críticas**
- Verificação da exposição de sistemas industriais (SCADA/ICS).
- Avaliação de segurança de hospitais, aeroportos e órgãos públicos.
- Localização de câmeras de vigilância desprotegidas.

#### **4. Investigação Digital e Análise Forense**
- Localização de servidores suspeitos usados em ataques.
- Identificação de dispositivos comprometidos por malware.
- Rastreio de infraestrutura usada por hackers.

---

### **Como Usar o Shodan**
#### **1. Criando uma Conta**
Para acessar a versão completa do Shodan, é necessário criar uma conta no site oficial: [https://www.shodan.io/](https://www.shodan.io/).

#### **2. Fazendo Buscas Básicas**
A busca no Shodan funciona de maneira similar ao Google, mas aceita filtros avançados para refinar os resultados. Alguns exemplos:

- `apache` → Mostra servidores web Apache expostos.
- `port:22` → Lista dispositivos com SSH aberto.
- `country:BR` → Filtra dispositivos no Brasil.
- `city:São Paulo` → Mostra dispositivos em uma cidade específica.
- `org:"Google LLC"` → Filtra dispositivos de uma empresa específica.
- `os:Windows` → Busca servidores Windows acessíveis.

#### **3. Usando Filtros Avançados**
Algumas consultas combinadas podem fornecer informações mais específicas:

- `port:3389 country:BR` → Mostra servidores RDP (Remote Desktop) no Brasil.
- `product:"MongoDB"` → Encontra bancos de dados MongoDB expostos.
- `ssl:"Tesla Motors"` → Busca certificados SSL da Tesla.
- `before:2023-01-01` → Mostra dispositivos indexados antes de 2023.

#### **4. API do Shodan**
O Shodan oferece uma API para automação e integração com outras ferramentas. Com ela, é possível:

- Criar alertas de exposição de dispositivos.
- Automatizar varreduras em redes empresariais.
- Desenvolver scripts para monitoramento contínuo.

---

### **Versões e Planos do Shodan**
O Shodan oferece diferentes níveis de acesso:

- **Gratuito** → Permite algumas buscas básicas e acesso limitado.
- **Shodan Membership ($49 – pagamento único)** → Permite mais consultas e acesso a relatórios mais completos.
- **Shodan API ($69/mês)** → Acesso completo à API para integração.
- **Shodan Enterprise** → Versão corporativa, customizável para grandes organizações.

---

### **Riscos e Ética no Uso do Shodan**
Embora seja uma ferramenta poderosa para segurança cibernética, o Shodan também pode ser usado para fins maliciosos, como a exploração de dispositivos vulneráveis. No entanto, o acesso e o uso do Shodan devem seguir normas éticas e legais:

✅ **Permitido**:
- Uso para auditorias de segurança próprias ou autorizadas.
- Pesquisa acadêmica e profissional de cibersegurança.
- Monitoramento de infraestrutura para evitar ataques.

❌ **Proibido**:
- Invasão de dispositivos sem autorização (crime em diversos países).
- Exploração de vulnerabilidades para obter acesso indevido.
- Uso para espionagem ou coleta de dados sigilosos sem permissão.

A ferramenta deve ser usada com responsabilidade e dentro dos limites legais.

---

### **Conclusão**
O **Shodan** é uma ferramenta essencial para segurança cibernética e inteligência digital, permitindo encontrar e analisar dispositivos conectados à internet. Seu uso adequado pode ajudar a proteger infraestruturas críticas, identificar vulnerabilidades e melhorar a segurança de redes. No entanto, é crucial seguir boas práticas e evitar o uso indevido para não violar leis de privacidade e segurança da informação.
