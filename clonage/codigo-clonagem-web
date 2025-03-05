from selenium import webdriver

driver = webdriver.Chrome()
driver.get("https://www.correios.com.br/")

with open("pagina.html", "w", encoding="utf-8") as f:
    f.write(driver.page_source)

driver.quit()
