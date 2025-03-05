# Explicação do código:
```markdown
# Explicação do Código Selenium para Obtenção do HTML de uma Página Web

Este script Python utiliza a biblioteca Selenium para automatizar a abertura de um navegador Chrome, acessar um site específico (no caso, os Correios do Brasil) e salvar o código-fonte HTML da página em um arquivo local.

## Pré-requisitos

* **Python:** Certifique-se de que o Python esteja instalado em seu sistema.
* **Selenium:** Instale a biblioteca Selenium usando o pip:
    
    ```bash
    pip install selenium
    ```
    
* **ChromeDriver:** Baixe o ChromeDriver correspondente à sua versão do Chrome e certifique-se de que ele esteja no PATH do seu sistema.

## Código

```python
from selenium import webdriver

driver = webdriver.Chrome()
driver.get("[https://www.correios.com.br/](https://www.correios.com.br/)")

with open("pagina.html", "w", encoding="utf-8") as f:
    f.write(driver.page_source)

driver.quit()
```

## Explicação Detalhada

1.  **Importação da Biblioteca:**
    
    ```python
    from selenium import webdriver
    ```
    
    * Importa o módulo `webdriver` da biblioteca Selenium, que permite controlar navegadores web.
2.  **Instanciação do Driver:**
    
    ```python
    driver = webdriver.Chrome()
    ```
    
    * Cria uma instância do driver do navegador Chrome. Isso inicia uma nova sessão do navegador.
3.  **Acessando a URL:**
    
    ```python
    driver.get("[https://www.correios.com.br/](https://www.correios.com.br/)")
    ```
    
    * Instrui o navegador Chrome a abrir a URL especificada (o site dos Correios).
4.  **Abertura e Escrita do Arquivo:**
    
    ```python
    with open("pagina.html", "w", encoding="utf-8") as f:
        f.write(driver.page_source)
    ```
    
    * Abre um arquivo chamado `pagina.html` no modo de escrita (`"w"`).
    * `encoding="utf-8"` garante que caracteres especiais sejam salvos corretamente.
    * `driver.page_source` obtém o código-fonte HTML da página.
    * `f.write()` escreve o código-fonte no arquivo.
5.  **Fechamento do Navegador:**
    
    ```python
    driver.quit()
    ```
    
    * Fecha a sessão do navegador Chrome e encerra o processo do ChromeDriver.

## Uso

1.  Certifique-se de ter todos os pré-requisitos instalados.
2.  Salve o código como um arquivo `.py` (por exemplo, `obter_html.py`).
3.  Execute o script a partir da linha de comando:
    
    ```bash
    python obter_html.py
    ```
    
4.  Um arquivo chamado `pagina.html` será criado no mesmo diretório do script, contendo o código HTML da página dos Correios.

## Observações

* Este script pode ser adaptado para acessar qualquer página web, bastando alterar a URL em `driver.get()`.
* O arquivo ChromeDriver deve ser compativel com a versão do seu navegador chrome.
* Este script pode ser usado para web scraping, análise de páginas web ou testes automatizados.
