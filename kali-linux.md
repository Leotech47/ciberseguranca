### **Guia Completo para Instalar e Rodar o Kali Linux na Oracle VM VirtualBox**  

Kali Linux é uma distribuição baseada em Debian, amplamente usada para testes de penetração e segurança cibernética. A instalação em uma **máquina virtual (VM)** com a **Oracle VM VirtualBox** permite rodá-lo sem modificar o sistema principal, garantindo segurança e praticidade.

---

## **1. Requisitos para a Instalação**
Antes de iniciar a instalação, verifique se seu computador atende aos requisitos mínimos:

### **Hardware Necessário**
✅ **Processador:** Dual-core ou superior (Intel/AMD)  
✅ **Memória RAM:** Pelo menos 4GB (recomendado 8GB+)  
✅ **Espaço em disco:** 25GB ou mais  
✅ **Suporte a virtualização:** Ative a virtualização na BIOS/UEFI (**VT-x** para Intel ou **AMD-V** para AMD)  

### **Softwares Necessários**
1. **Oracle VM VirtualBox** – Pode ser baixado no site oficial:  
   🔗 [https://www.virtualbox.org/](https://www.virtualbox.org/)  
2. **Kali Linux ISO ou imagem pronta para VirtualBox** – Disponível no site oficial do Kali Linux:  
   🔗 [https://www.kali.org/get-kali/](https://www.kali.org/get-kali/)  

---

## **2. Instalando o Oracle VM VirtualBox**
1. Baixe o **Oracle VM VirtualBox** do site oficial.  
2. Execute o instalador (`VirtualBox-x.x.x.exe`).  
3. Durante a instalação, mantenha todas as configurações padrão e clique em **Next > Install**.  
4. Após a instalação, abra o VirtualBox e siga para a criação da máquina virtual.

---

## **3. Criando uma Máquina Virtual para o Kali Linux**
### **Passo 1: Criar uma nova VM**
1. No VirtualBox, clique em **"Novo"** para criar uma nova máquina virtual.  
2. Escolha um nome para a VM, como **"Kali Linux"**.  
3. Em **Tipo**, selecione **Linux**.  
4. Em **Versão**, escolha **Debian (64-bit)** (pois o Kali é baseado no Debian).  
5. Clique em **Próximo**.

### **Passo 2: Configurar a Memória RAM**
- Defina pelo menos **4096 MB (4GB)** de RAM.  
- Se possível, use **8192 MB (8GB)** para melhor desempenho.  
- Evite ultrapassar 50% da memória total do seu computador.

### **Passo 3: Criar um Disco Virtual**
1. Escolha **Criar um disco rígido virtual agora** e clique em **Criar**.  
2. Selecione **VDI (VirtualBox Disk Image)** e clique em **Avançar**.  
3. Escolha **Dinamicamente alocado** e clique em **Avançar**.  
4. Defina pelo menos **25GB** de espaço (ou mais, se necessário).  
5. Clique em **Criar**.

---

## **4. Configurando a VM Antes de Instalar o Kali Linux**
1. **Selecione a VM criada** e clique em **Configurações**.  
2. Vá para **Sistema > Processador** e aumente para **2 núcleos** (ou mais, se possível).  
3. Em **Armazenamento**, clique em **Vazio > Atributos > Escolher um disco** e selecione o **arquivo ISO do Kali Linux** que você baixou.  
4. Em **Rede**, altere o adaptador para **Modo Bridge** para que o Kali tenha acesso à rede real.  
5. Clique em **OK** para salvar as configurações.

---

## **5. Instalando o Kali Linux**
### **Passo 1: Iniciar a Máquina Virtual**
1. Com a VM selecionada, clique em **Iniciar**.  
2. No menu de inicialização do Kali Linux, escolha **Graphical Install**.  

### **Passo 2: Configurar o Idioma e Teclado**
1. Escolha o idioma **Português (Brasil)** (ou o idioma desejado).  
2. Selecione o layout do teclado.  

### **Passo 3: Configurar Rede e Usuário**
1. Digite um nome para o computador.  
2. Crie um usuário e senha (anote para não esquecer).  

### **Passo 4: Particionamento de Disco**
1. Escolha **Guiado - usar todo o disco** e confirme.  
2. Selecione **Finalizar** e **Continuar**.  

### **Passo 5: Instalar o Sistema**
1. Aguarde a instalação do sistema base.  
2. Quando solicitado, escolha **Sim** para instalar o GRUB.  
3. Após a instalação, reinicie a VM.  

---

## **6. Finalizando e Rodando o Kali Linux**
Após a reinicialização, remova o **arquivo ISO** da unidade de CD/DVD para evitar que a VM reinicie o instalador.

1. Faça login com o usuário e senha definidos.  
2. Atualize o sistema com:  
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```
3. Instale as **VirtualBox Guest Additions** para melhorar a integração da VM:  
   ```bash
   sudo apt install -y virtualbox-guest-x11
   reboot
   ```

Agora o **Kali Linux está pronto para uso** dentro da Oracle VM VirtualBox! 🚀

