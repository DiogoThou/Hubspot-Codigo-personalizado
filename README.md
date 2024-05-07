# Códigos personalizados para Hubspot
### Codigos publicos do Hubspot - Usar dentro dos workflows (necessário a função de Hub Operation) <3


Dúvidas só falar comigo aqui > https://diovofrito.com/s/chama


-------------------------------------------------------------------


## 1 - Formatar CNPJ da empresa - [Codigo completo](https://github.com/DiogoThou/hubspot/blob/main/Formatar%20CNPJ%20da%20empresa) Node16x

**Instruções:**

1 - Criar um [aplicativo privado](https://br.developers.hubspot.com/docs/api/private-apps) no hubspot, copiar o token e inserir no codigo em "VALOR DO SEU TOKEN";

2 - Substituir no codigo o campo "cnpj_new" pelo nome interno do seu campo de CNPJ no hubspot;

3 - [Configuração de Propriedade para incluir no código (link)](https://diovofrito.com/blog/wp-content/uploads/2024/05/formatarcnpj1.png)

4 - [Configuração da saida de dados (link)](https://diovofrito.com/blog/wp-content/uploads/2024/05/formatarcnpj2.png)

5 - Codigo funcionando <3 

-------------------------------------------------------------------

## 2 - Copiar nome e sobrenome com base no e-mail - [Codigo completo](https://github.com/DiogoThou/hubspot/blob/main/Copiar%20nome%20da%20pessoa%20com%20base%20no%20e-mail) Node16x

Existem casos, como newsletters, em que temos apenas o e-mail da pessoa dentro do HubSpot. O código ajuda a copiar o nome da pessoa com base no e-mail. Por exemplo, para o e-mail "diogo.souza@SuaEmpresa.com", o código separa tudo o que está entre pontos (.) e salva como nome e sobrenome. No final, ficaria: Nome: Diogo - Sobrenome: Souza.


**Instruções:**

1 - Não é necessário um aplicativo privado. Criar um bloco de codigo personalizado e inserir o codigo acima.

2 - Configurar as propriedades para [incluir no codigo](https://diovofrito.com/blog/wp-content/uploads/2024/05/salvarnome1.png) - e as propriedades de [saída de dados](https://diovofrito.com/blog/wp-content/uploads/2024/05/salvarnome2.png);

3 - SALVAR! Criar um bloco de "Formatar dados" logo abaixo e [configurar desta maneira](https://diovofrito.com/blog/wp-content/uploads/2024/05/salvarnome-formatar1.png);

5 - SALVAR! Criar um bloco para copiar o valor [formatado para o campo de nome/sobrenome](https://diovofrito.com/blog/wp-content/uploads/2024/05/salvarnome-formatar2.png);

6 - Codigo funcionando <3 [teste](https://diovofrito.com/blog/wp-content/uploads/2024/05/salvarnome3.png)

-------------------------------------------------------------------
