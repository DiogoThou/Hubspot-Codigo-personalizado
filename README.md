# Códigos personalizados para Hubspot
### Codigos publicos do Hubspot - Usar dentro dos workflows (necessário a função de Hub Operation) <3


Dúvidas só falar comigo aqui > https://diovofrito.com/s/chama


> [!CAUTION]
> NÃO COMPARTILHE O TOKEN DE API COM NINGUÉM. ISSO PODE CAUSAR SÉRIOS PROBLEMAS AO SEU CRM!

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

## 3 - Associar contato com empresa com base em uma propriedade - [Codigo completo](https://diovofrito.com/s/git-cliente) Node16x

Este código ajuda você a associar contatos com empresas com base em uma propriedade específica (pode ser o CNPJ, campo de identificação do cliente, que neste código chamamos de "Account_ID" ou qualquer outra propriedade que precisa ser igual no contato e na empresa). Caso a propriedade não seja igual, ele vai criar uma nova empresa para este contato já com este campo copiado para a empresa. 


**Instruções:**

1 - Criar um [aplicativo privado](https://br.developers.hubspot.com/docs/api/private-apps) no hubspot, copiar o token e inserir no codigo em "VALOR DO SEU TOKEN";

2 - [Configuração de Propriedade para incluir no código (link)](https://diovofrito.com/blog/wp-content/uploads/2024/05/associarcontatocomempresa.png);

4 - Testar um contato e uma empresa onde ambos tenham a propriedade (que você definiu) com os mesmos valores;

5 - Codigo funcionando <3 

EXTRA - Caso você queira usar outro campo no lugar de "account_ID" basta substituir este valor pelo nome interno do seu campo no codigo e em toda instrução!

-------------------------------------------------------------------

## 4 - Associar contato com empresa com base no "nome da empresa" - [Codigo completo](https://github.com/DiogoThou/hubspot/blob/main/Associar%20empresa%20ao%20contato%20quando%20o%20%22nome%20da%20empresa%22%20for%20igual) Node16x

Existem casos em que o contato não tem um site ou o e-mail dele é gratuito. Quando é assim, o HubSpot não cria uma empresa para ele automaticamente. Isso acaba prejudicando análises relacionadas às empresas do Hub (como quantidade de MQLs/SQLs/clientes). O código acima ajuda você a criar uma empresa automaticamente para esses contatos. Ele procura com base no campo "Nome da empresa" nativo do Hub. Caso exista uma empresa no Hub com o mesmo nome, ele vai associar automaticamente com o contato. Caso contrário, ele vai pegar o "Nome da empresa" e criar uma nova empresa com esse valor... e associar no final!


**Instruções:**

1 - Criar um [aplicativo privado](https://br.developers.hubspot.com/docs/api/private-apps) no hubspot, copiar o token e inserir no codigo em "VALOR DO SEU TOKEN";

2 - Configurar a [Saídas de dados](https://diovofrito.com/blog/wp-content/uploads/2024/05/associarcontatoempresamesmonome.png) para ter o retorno caso o codigo de positivo;

4 - Testar em um contato que não tenha uma empresa associada e que o campo "nome da empresa" esteja preenchido;

5 - Codigo funcionando <3 

-------------------------------------------------------------------

## 5 - Formatar telefone/celular do contato - [Codigo completo](https://github.com/DiogoThou/Hubspot-Codigo-personalizado/blob/main/Formatar%20celular%20do%20contato) Node16x

A ideia é formatar o celular do contato, assim evitando erros na hora de fazer uma chamada ou uma comunicação via WhatsApp. No código, estou usando o "mobilePhone", mas também daria para usar com o telefone. Basta alterar esta variável para "phone".
A ideia é caso o telefone esteja desformatado, formatar para o padrão do HubSpot +55-00-90000-0000 - e caso seja identificado que é um telefone e não um celular, formatar como +55-00-0000-0000.


**Instruções:**

1 - Configurar as propriedades para [incluir no codigo](https://diovofrito.com/blog/wp-content/uploads/2024/05/formatartelefone.png) - e as propriedades de [saída de dados](https://diovofrito.com/blog/wp-content/uploads/2024/05/formatartelefone1.png);

2 - SALVAR! Criar um campo de "copiar valor da propriedade" e [configurar desta maneira](https://diovofrito.com/blog/wp-content/uploads/2024/05/formatartelefone2.png) para receber o resultado de phone; 

4 - Testar em um campo de celular que não esteja formatado;

5 - Codigo funcionando <3 

-------------------------------------------------------------------



