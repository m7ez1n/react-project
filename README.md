# Um projeto bem simples em react :octocat:

## Imagem das duas páginas da aplicação :computer: :mortar_board:

![Captura de Tela (2)](https://user-images.githubusercontent.com/44484286/65918218-7bf5d080-e3af-11e9-8e30-81fd5d407fb9.png)


Esse projeto está usando a API do github para pegar informações de repositórios,é algo bem simples. Você pode adicionar um repositório que existe no github e também pode ver mais sobre ele, em outra página. No caso ele mostra a foto do criador a descrição e suas issues abertas.

## Próximas mudanças :squirrel:

### Funcionalidades :grin:

#### Captando erros :dizzy_face:

Adicione um ```try/catch``` por volta do código presente na função ```handleSubmit``` presente no componente ```Main``` e caso um repositório não seja encontrado na API do Github adicione uma borda vermelha por volta do input em que o usuário digitou o nome do repositório.

#### Repositório duplicado :page_facing_up:

Antes de fazer a chamada à API na função ```handleSubmit``` faça uma verificação para ver se o repositório não está duplicado, ou seja, se ele ainda não existe no estado de ```repositories```.

Caso exista, dispare um erro, e com isso o código cairá no catch do ```try/catch``` criado na funcionalidade anterior.

```js
throw new Error('Repositório duplicado');
```

#### Filtro de estado :mag:

Adicione um filtro de estado na listagem de Issues que criamos no detalhe do repositório. O estado representa se a issue está em aberto, fechada ou uma opção para exibir todas.

Exemplos de requisição:

```js
https://api.github.com/repos/rocketseat/unform/issues?state=all
https://api.github.com/repos/rocketseat/unform/issues?state=open
https://api.github.com/repos/rocketseat/unform/issues?state=closed
```

A documentação está [nesse link](https://developer.github.com/v3/issues/#parameters-1);


#### Paginação :paperclip:

Adicione paginação nas issues listadas no detalhe do repositório. A API do Github lista no máximo 30 issues por página e você pode controlar o número da página atual por um parâmetro no endereço da requisição:

```https://api.github.com/repos/rocketseat/unform/issues?page=2```

Adicione apenas um botão de próxima página e página anteior. O botão de página anterior deve ficar desativado na primeira página.

<h2 align="center">
  Acessem a He4rt :purple_heart:
</h2>

<h3 align="center">
  <img src="https://heartdevs.com/wp-content/uploads/2018/12/logo.png" width="215"><br>
    Visite nosso discord, vamo codar junto!! :godmode:
	<a href="https://discord.io/He4rt" target="_blank">
	<img src="https://discordapp.com/api/guilds/452926217558163456/embed.png" alt="Discord server"/></a><br>
</h3>

[Twitter He4rt](https://twitter.com/He4rtDevs)

[Meu Twitter](https://twitter.com/m7AeiHe4rt)