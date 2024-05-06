from selenium import webdriver

driver = webdriver.Chrome()  # Inicia o browser
driver.get('https://www.python.org/')  # Acessar a URL especificada
driver.find_element_by_css_selector('#id-search-field').send_keys("python")  # Digita o texto "python" no input
driver.find_element_by_css_selector('#submit').click()  # Clica no botão de submit
driver.quit()  # Encerra o browser


# language: pt

Funcionalidade: realizar pesquisa no Google
  
  # Contexto são ações que serão executadas antes de cada cenário.
  Contexto: acessar página de teste
    Dado que acesso a página do Google

  Cenário: acessar página do Google e realizar pesquisa
    Dado que preencho o campo de pesquisa com Python
    Quando clico no botão de pesquisar
    Então devo visualizar os resultados
