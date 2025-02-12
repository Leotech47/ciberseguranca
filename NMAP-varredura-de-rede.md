**Varredura de rede** é o processo de identificar dispositivos, serviços e vulnerabilidades em uma rede de computadores. O objetivo principal é mapear e avaliar os ativos e a segurança da rede, buscando potenciais brechas ou falhas que possam ser exploradas por atacantes.

### Como realizar a varredura de rede
1. **Planejamento**: Definir o escopo da varredura, como quais endereços IP ou sub-redes serão escaneados.
2. **Escolha de técnicas e ferramentas**: Selecionar as ferramentas apropriadas e as técnicas de varredura (passivas ou ativas).
3. **Execução**: Realizar a varredura na rede e analisar os resultados.
4. **Análise de resultados**: Identificar dispositivos, serviços, portas abertas, vulnerabilidades, etc.
5. **Ação corretiva**: Tomar as medidas necessárias, como a correção de vulnerabilidades.

### Técnicas utilizadas
1. **Varredura de portas**: Identifica portas abertas em dispositivos na rede para determinar quais serviços estão disponíveis.
2. **Varredura de host**: Identifica os dispositivos conectados à rede (via ICMP ou ARP, por exemplo).
3. **Varredura de vulnerabilidades**: Detecta falhas de segurança e possíveis pontos de exploração.
4. **Varredura passiva**: Coleta informações sem interagir diretamente com os dispositivos, evitando detecção (ex: monitoramento de tráfego).
5. **Varredura ativa**: Envia pacotes de rede para dispositivos e observa as respostas, permitindo a identificação de ativos de forma mais precisa.

### Ferramentas disponíveis
1. **Nmap**: Uma das ferramentas mais populares para varredura de portas e descoberta de rede.
2. **OpenVAS**: Ferramenta de varredura de vulnerabilidades, mais voltada para a detecção de falhas de segurança.
3. **Wireshark**: Ferramenta de análise de pacotes que pode ser usada para monitoramento de tráfego e varredura passiva.
4. **Nessus**: Ferramenta comercial para scanner de vulnerabilidades.
5. **Zenmap**: Interface gráfica para o Nmap, facilitando o uso para iniciantes.
6. **Masscan**: Ferramenta de varredura rápida e eficiente, especialmente para varredura de grandes redes.

Essas ferramentas são essenciais para administrar, testar e fortalecer a segurança de redes e sistemas.

A instalação e o uso do **Nmap** variam dependendo do sistema operacional que você está utilizando. Aqui estão as instruções detalhadas para diferentes sistemas operacionais.

### **1. Instalando o Nmap no Linux (Ubuntu/Debian)**

No Ubuntu ou Debian, você pode instalar o Nmap usando o **APT** (Advanced Package Tool).

#### Passos:
1. **Abra o terminal**.
2. **Atualize os repositórios de pacotes**:
   ```bash
   sudo apt update
   ```
3. **Instale o Nmap**:
   ```bash
   sudo apt install nmap
   ```

Após a instalação, você pode verificar a versão instalada para confirmar a instalação:

```bash
nmap --version
```

### **2. Instalando o Nmap no macOS**

No macOS, a maneira mais simples de instalar o Nmap é utilizando o **Homebrew** (gerenciador de pacotes).

#### Passos:
1. **Instale o Homebrew** (caso ainda não tenha instalado). Se já o tiver, pule esta etapa. Execute no terminal:
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. **Instale o Nmap** usando o Homebrew:
   ```bash
   brew install nmap
   ```

Após a instalação, você pode verificar a versão do Nmap com o seguinte comando:

```bash
nmap --version
```

### **3. Instalando o Nmap no Windows**

No Windows, a maneira mais fácil de instalar o Nmap é usando o **instalador oficial** do Nmap para Windows.

#### Passos:
1. **Baixe o instalador** do Nmap no [site oficial do Nmap](https://nmap.org/download.html).
   - Clique na opção "Windows binaries" e baixe o instalador `.exe`.

2. **Execute o instalador**:
   - Durante a instalação, você pode escolher se deseja instalar o Nmap, Zenmap (interface gráfica), ou ambos.
   - Certifique-se de que a opção "Add Nmap to system PATH" esteja marcada, isso permitirá que você execute o Nmap de qualquer prompt de comando.

3. **Conclua a instalação** e depois abra o **Prompt de Comando** (ou PowerShell).
4. **Verifique a instalação**:
   ```bash
   nmap --version
   ```

### **4. Utilizando o Nmap**

Depois de instalar o Nmap, você pode começar a utilizá-lo diretamente no terminal (Linux/macOS) ou no Prompt de Comando (Windows). Aqui estão alguns comandos básicos para começar:

#### **Exemplo 1: Descobrir hosts ativos em uma rede**
```bash
nmap -sn 192.168.1.0/24
```
- Este comando fará um **ping sweep** para descobrir quais dispositivos estão ativos na rede `192.168.1.0/24`.

#### **Exemplo 2: Varredura de portas específicas**
```bash
nmap -p 80,443 192.168.1.10
```
- Este comando verifica as portas **80** (HTTP) e **443** (HTTPS) no host com o IP `192.168.1.10`.

#### **Exemplo 3: Varredura de serviços e versões**
```bash
nmap -sV 192.168.1.10
```
- Este comando identifica os **serviços e suas versões** nas portas abertas do host `192.168.1.10`.

#### **Exemplo 4: Detecção de sistema operacional**
```bash
nmap -O 192.168.1.10
```
- Este comando tenta identificar o **sistema operacional** do host `192.168.1.10`.

### **Usando o Zenmap (Interface Gráfica)**

Se você preferir uma interface gráfica para usar o Nmap, pode usar o **Zenmap**, que é a versão GUI (interface gráfica de usuário) do Nmap. Zenmap é instalado automaticamente junto com o Nmap em sistemas Windows, Linux e macOS.

#### Passos para usar o Zenmap:
1. Abra o **Zenmap** (geralmente localizado no menu de aplicativos ou na lista de programas).
2. No campo **"Target"** (Alvo), insira o endereço IP ou o intervalo de IP que você deseja escanear (ex: `192.168.1.10` ou `192.168.1.0/24`).
3. No campo **"Profile"** (Perfil), selecione o tipo de varredura que deseja realizar (por exemplo, "Intense Scan").
4. Clique em **"Scan"** (Escanear).
5. O Zenmap exibirá o resultado da varredura de maneira gráfica, mostrando as portas abertas, serviços detectados e informações sobre o sistema.

---

### **Conclusão**

Agora que você tem o Nmap instalado em seu sistema, pode começar a utilizá-lo para realizar varreduras de rede, detectar vulnerabilidades e mapear dispositivos. Ele é uma ferramenta poderosa para administradores de rede, profissionais de segurança e qualquer pessoa que precise realizar auditorias em redes e sistemas.

Aqui estão três exemplos práticos detalhados de como usar a ferramenta **Nmap** para realizar varreduras em uma rede:

### 1. **Descoberta de Hosts na Rede (Ping Sweep)**
O primeiro passo para realizar uma análise de rede é identificar quais dispositivos estão ativos. Com a varredura de "ping", é possível descobrir quais hosts estão respondendo dentro de uma faixa de IPs.

#### Comando:
```bash
nmap -sn 192.168.1.0/24
```

- **Explicação**: O comando `-sn` (ping scan) faz com que o Nmap realize uma varredura simples de descoberta de hosts sem realizar a varredura de portas.
- **192.168.1.0/24**: Este é o intervalo de IPs da rede local (sub-rede). O Nmap tentará fazer ping em todos os IPs de 192.168.1.1 a 192.168.1.254 para verificar quais estão ativos.
- **Resultado**: O Nmap retorna uma lista de hosts ativos (que responderam ao ping), mostrando o endereço IP e o tempo de resposta.

**Exemplo de saída**:
```
Nmap scan report for 192.168.1.1
Host is up (0.0012s latency).
Nmap scan report for 192.168.1.5
Host is up (0.0009s latency).
Nmap scan report for 192.168.1.10
Host is up (0.0014s latency).
```

---

### 2. **Varredura de Portas Específicas em um Host**
Agora, imagine que você deseja descobrir quais portas estão abertas em um dispositivo específico. Suponha que o endereço IP do host seja `192.168.1.10`. O comando a seguir verifica se as portas comuns de um servidor web (80 e 443) estão abertas.

#### Comando:
```bash
nmap -p 80,443 192.168.1.10
```

- **Explicação**: O parâmetro `-p` especifica as portas que você deseja verificar. Neste caso, estamos verificando as portas 80 (HTTP) e 443 (HTTPS) do host `192.168.1.10`.
- **Resultado**: O Nmap verifica se as portas 80 e 443 estão abertas e retorna o status delas.

**Exemplo de saída**:
```
Starting Nmap 7.91 ( https://nmap.org ) at 2025-02-12 14:00 UTC
Nmap scan report for 192.168.1.10
Host is up (0.0008s latency).
PORT    STATE SERVICE
80/tcp  open  http
443/tcp open  https

Nmap done: 1 IP address (1 host up) scanned in 1.60 seconds
```

---

### 3. **Varredura Completa de Serviços e Versões**
Se você deseja realizar uma análise mais detalhada de um host, incluindo a descoberta de serviços em execução e suas versões, você pode usar o parâmetro `-sV` para fazer isso.

#### Comando:
```bash
nmap -sV 192.168.1.10
```

- **Explicação**: O parâmetro `-sV` solicita ao Nmap a detecção dos serviços e suas versões. Isso é útil para identificar quais serviços estão rodando em quais portas, além de coletar informações sobre as versões dessas aplicações.
- **Resultado**: O Nmap retorna uma lista detalhada das portas abertas, serviços em execução e versões encontradas.

**Exemplo de saída**:
```
Starting Nmap 7.91 ( https://nmap.org ) at 2025-02-12 14:05 UTC
Nmap scan report for 192.168.1.10
Host is up (0.0010s latency).
Not shown: 996 closed ports
PORT     STATE SERVICE    VERSION
22/tcp   open  ssh        OpenSSH 7.6p1 Ubuntu 4 (Ubuntu Linux; protocol 2.0)
80/tcp   open  http       Apache httpd 2.4.29 ((Ubuntu))
443/tcp  open  ssl/http   Apache httpd 2.4.29 ((Ubuntu))
3306/tcp open  mysql      MySQL 5.7.32-0ubuntu0.18.04.1
8080/tcp open  http-proxy Squid http proxy 3.5.27

Nmap done: 1 IP address (1 host up) scanned in 10.00 seconds
```

**Interpretação**:
- **Porta 22/tcp**: Está aberta e executando o serviço SSH (OpenSSH 7.6p1).
- **Porta 80/tcp**: Está aberta e executando o Apache HTTPD 2.4.29.
- **Porta 443/tcp**: Está aberta e também executando o Apache HTTPD, mas com SSL (HTTPS).
- **Porta 3306/tcp**: Está aberta e executando o MySQL 5.7.
- **Porta 8080/tcp**: Está aberta e executando o Squid como proxy HTTP.

Esse tipo de varredura é importante para determinar a segurança de uma máquina, uma vez que a versão do serviço pode ser vulnerável a exploits conhecidos.

---

Para instalar o **Nmap** em uma **máquina virtual** (VM) usando o **Oracle VM VirtualBox**, o processo de instalação depende do sistema operacional que você está utilizando na VM. Vou guiar você por três possíveis cenários: **Ubuntu/Debian**, **CentOS/RHEL** e **Windows**.

### **1. Instalando o Nmap em uma VM com Ubuntu/Debian**

Se você estiver usando uma VM rodando uma distribuição baseada no Debian (como o Ubuntu), você pode usar o gerenciador de pacotes **APT** para instalar o Nmap.

#### Passos:
1. **Abra o terminal** na sua máquina virtual (VM).
2. **Atualize os repositórios de pacotes**:
   ```bash
   sudo apt update
   ```
3. **Instale o Nmap**:
   ```bash
   sudo apt install nmap
   ```
4. **Verifique a instalação**:
   Após a instalação, verifique se o Nmap foi instalado corretamente com o comando:
   ```bash
   nmap --version
   ```

### **2. Instalando o Nmap em uma VM com CentOS/RHEL**

Se você estiver utilizando uma distribuição baseada no **Red Hat**, como **CentOS**, o **YUM** ou **DNF** (dependendo da versão) será o gerenciador de pacotes.

#### Passos:
1. **Abra o terminal** na sua máquina virtual.
2. **Instale o Nmap** usando o **DNF** ou **YUM**:
   - Para versões mais recentes do CentOS/RHEL (com DNF):
     ```bash
     sudo dnf install nmap
     ```
   - Para versões mais antigas (usando YUM):
     ```bash
     sudo yum install nmap
     ```
3. **Verifique a instalação**:
   ```bash
   nmap --version
   ```

### **3. Instalando o Nmap em uma VM com Windows**

Caso você esteja utilizando o **Windows** na sua máquina virtual, você pode usar o **instalador oficial** do Nmap para Windows.

#### Passos:
1. **Baixe o instalador**:
   - Acesse o [site oficial do Nmap](https://nmap.org/download.html).
   - Na seção "Windows binaries", baixe o instalador `.exe` mais recente.
   
2. **Execute o instalador**:
   - Após o download, execute o arquivo `.exe`.
   - Durante a instalação, você pode escolher se deseja instalar o **Nmap**, o **Zenmap** (interface gráfica) e o **Ncat** (ferramenta de rede adicional).
   - **Certifique-se de selecionar a opção "Add Nmap to system PATH"**, isso permitirá que você execute o Nmap diretamente de qualquer prompt de comando.

3. **Finalização da instalação**:
   - Conclua a instalação e abra o **Prompt de Comando** ou **PowerShell**.

4. **Verifique a instalação**:
   No Prompt de Comando, execute:
   ```bash
   nmap --version
   ```

### **Configurando Rede na VM**

Certifique-se de que a sua máquina virtual (VM) tenha a configuração de rede adequada para acessar a rede à qual você deseja escanear. No **Oracle VM VirtualBox**, você pode usar as seguintes configurações de rede:

1. **Modo de Rede:**
   - Se a sua VM deve se conectar à sua rede local ou à internet, escolha **"Bridged Adapter"** (Adaptador em Ponte).
   - Se você deseja que a VM tenha uma rede isolada entre a máquina host e a VM, escolha **"Internal Network"** ou **"Host-Only Adapter"**.

2. **Verifique a conectividade:**
   Antes de realizar qualquer varredura com o Nmap, teste a conectividade da sua VM com a rede:
   ```bash
   ping 8.8.8.8  # Para testar a conectividade com a internet
   ping 192.168.x.x  # Para testar a conectividade com outros dispositivos da rede local
   ```

### **4. Executando o Nmap na VM**

Após a instalação do Nmap, você pode começar a utilizá-lo na VM para fazer varreduras de rede. A partir da linha de comando (ou terminal na VM), use os comandos do Nmap como descrito anteriormente para descobrir hosts ativos, realizar varreduras de portas, e identificar serviços e vulnerabilidades.

#### Exemplo básico para descobrir hosts ativos:
```bash
nmap -sn 192.168.1.0/24
```

#### Exemplo para varredura de portas:
```bash
nmap -p 80,443 192.168.1.10
```

### **Conclusão**

Com esses passos, você deve ser capaz de instalar o Nmap em sua máquina virtual, seja ela rodando Linux ou Windows. Certifique-se de configurar corretamente a rede da VM para permitir que ela acesse os dispositivos ou serviços que você deseja escanear.



Esses exemplos são apenas alguns dos muitos usos do Nmap, e a ferramenta pode ser personalizada para atender a diferentes necessidades de varredura de rede.

