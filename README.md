# AnimeWallet

API do Projeto AnimeWallet 

### O que usamos:
- Java

## Requisitos

- [ ] CRUD Usuários
- [ ] Autenticação 
- [ ] CRUD Avaliações

### Endpoints
- [Minha Conta](#minha-conta)
- [Listar Todos os Animes](#listar-todos-os-animes)
- [Listar Ranking de Animes](#listar-ranking-de-animes)
- [Realizar uma Avaliação]()

### Minha Conta
`GET` /minha-conta

Retorna os dados que o usuário cadastrou

#### Exemplo de Resposta
```js
[
    {
        "Usuário": "Vinicius"
        "e-mail": "vinicius@vinicius.com"
    }
]
```

---

### Listar Todos os Animes
`GET` /animes

Retorna uma lista com todos os animes cadastrados

#### Exemplo de Resposta
```js
[
    {
        "id": 1
        "Nome": "Jujutsu Kaisen"
    }
    {
        "id": 2
        "Nome": "Death Note"
    }
    {
        "id": 3
        "Nome": "My Hero Academia"
    }
]
```
![Captura de tela 2024-03-06 195748](https://github.com/vinioalmeida/AnimeWallet/assets/85771987/abaefdae-6a1f-4f63-8271-25ccfc0f1397)

---

### Listar Ranking de Animes
`GET` /Ranking

Retorna uma lista com os animes com melhores avaliações

#### Exemplo de Resposta
```js
[
    {
        "rank": 1
        "Nome": "Jujutsu Kaisen"
        "Score": 9.15
    } 
    {
        "rank": 2
        "Nome": "Death Note"
        "Score": 9.09
    }
    {
        "rank": 3
        "Nome": "My Hero Academia"
        "Score": 9.07
    }
]
```

---

### Realizar Avaliação
`POST` /animes/avaliação

#### Corpo da Requisição
|Campo|Tipo|Obrigatório|Descrição
|-----|----|-----------|---------
|Avaliação|String|❌|Avaliação do usuário para o anime correspondente

#### Exemplo de Requisição
```js
[
    {
        "Avaliação": "Achei esse anime muito, mas muito interessante. A cada episódio que assisto fico mais intrigado e curioso em saber o que vai acontecer."
    }
]
```

#### Exemplo de Resposta
```js
[
    {
        "id": 123
        "Avaliação": "Achei esse anime muito, mas muito interessante. A cada episódio que assisto fico mais intrigado e curioso em saber o que vai acontecer."
    }
]
```


