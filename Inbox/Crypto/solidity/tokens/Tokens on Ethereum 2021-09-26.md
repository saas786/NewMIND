---
type: paper
tags: 📥️/📜️/🩳/🗿
aliases:
  - 
cssclass: 
---



# Title: **[[Tokens on Ethereum 2021-09-26]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2021-09-26]]


A **_token_** на Эфириуме в основном только умный контракт , который следует несколько общих правил , а именно - он реализует стандартный набор функций , что все остальные лексемы контрактов на акцию, такие как `transferFrom(address _from, address _to, uint256 _tokenId)`и `balanceOf(address _owner)`.

Внутри смарт-контракта обычно есть отображение, `mapping(address => uint256) balances`которое отслеживает, сколько баланса имеет каждый адрес.

Таким образом, в основном токен - это просто контракт, который отслеживает, кто владеет каким количеством этого токена, и некоторые функции, чтобы эти пользователи могли передавать свои токены на другие адреса.