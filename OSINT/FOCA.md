### **FOCA – Ferramenta de Cibersegurança para OSINT e Análise de Metadados**

FOCA (Fingerprinting Organizations with Collected Archives) é uma ferramenta de código aberto utilizada para **coletar e analisar metadados de documentos** encontrados na internet. Desenvolvida pela empresa espanhola ElevenPaths, a FOCA é amplamente utilizada em testes de segurança cibernética, auditorias e investigações de inteligência de fontes abertas (OSINT – Open Source Intelligence).

---

## **Principais Funcionalidades do FOCA**
FOCA é especializada na análise de **documentos publicados online**, extraindo metadados que podem revelar informações sensíveis sobre uma organização, incluindo:

1. **Coleta e análise de metadados**  
   - Extrai informações de arquivos em formatos como **PDF, DOCX, XLSX, PPTX, ODT, JPG e outros**.  
   - Recupera **nomes de usuários**, **estruturas de rede**, **endereços IP internos**, **servidores**, **software utilizado**, entre outros.

2. **Pesquisa e indexação de documentos**  
   - Utiliza **motores de busca** como Google, Bing e DuckDuckGo para encontrar arquivos disponíveis publicamente.  
   - Também pode realizar pesquisas em diretórios web para localizar documentos não protegidos.

3. **Mapeamento de rede e infraestrutura**  
   - A partir dos metadados, FOCA pode inferir estruturas internas de TI, como **nomes de máquinas, endereços IP internos e domínios** utilizados por uma organização.

4. **Análise de vulnerabilidades**  
   - Com os dados extraídos, é possível identificar **sistemas desatualizados** e softwares vulneráveis, auxiliando na avaliação de riscos.

---

## **Exemplos Práticos de Utilização do FOCA**

### **1. Investigação de Metadados em Documentos Públicos**
Imagine que um analista de segurança deseja obter informações sobre a infraestrutura de uma empresa. Ele pode utilizar FOCA para pesquisar documentos da empresa na internet e analisar seus metadados.

**Passos:**  
1. Insere o domínio da empresa no FOCA.  
2. A ferramenta pesquisa documentos disponíveis publicamente.  
3. Os documentos são baixados e analisados automaticamente.  
4. FOCA extrai **nomes de usuários, versões de software, endereços IP internos** e outras informações valiosas.  

➡ **Exemplo real**: Um relatório financeiro em PDF publicado no site da empresa pode conter metadados revelando que foi criado por um usuário chamado "admin" em uma máquina chamada "servidor-corporativo". Isso já dá pistas sobre a estrutura da rede.

---

### **2. Coleta de Informações para Engenharia Social**
FOCA pode ser usada para **descobrir nomes de funcionários, endereços de e-mail e padrões de nomenclatura interna**, facilitando ataques de phishing.

**Exemplo:**  
- A ferramenta identifica que documentos são criados por usuários como “joao.silva@empresa.com” e “maria.souza@empresa.com”.  
- O atacante pode deduzir que a empresa usa o formato “nome.sobrenome@empresa.com” para os e-mails e criar e-mails falsos convincentes.

---

### **3. Mapeamento de Infraestrutura de uma Organização**
A análise de metadados pode revelar **endereços IP internos e servidores** de uma organização.

**Exemplo:**  
- Um documento Word pode conter a informação "Impressora_192.168.1.100", sugerindo que a empresa usa o esquema de IP interno **192.168.1.X**.  
- Esse dado pode ajudar a entender a configuração de rede e possíveis vulnerabilidades.

---

## **Conclusão**
FOCA é uma ferramenta poderosa para **inteligência de segurança cibernética**, ajudando tanto profissionais de segurança quanto invasores a identificar falhas e vulnerabilidades em organizações. Seu uso ético é fundamental para evitar vazamentos de informações sensíveis e garantir a segurança de dados.

Se utilizada corretamente, pode auxiliar equipes de segurança na **detecção de informações expostas** e na **mitigação de riscos**, reduzindo a superfície de ataque de uma organização.
