---
type: paper
tags: 📥️/📜️/🩳/🗿
aliases:
  - 
cssclass: 
---



# Title: **[[Storage and Memory 2021-09-23]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2021-09-23]]

В Solidity есть два места, где могут сохраняться переменные: в `storage` (хранилище) и в `memory` (памяти).

**_Хранилище_** используют, чтобы сохранить переменные в блокчейн навсегда. **_Память_** используют для временного хранения переменных, они стираются в промежутках, когда внешняя функция обращается к контракту. Это похоже на жесткий диск компьютера и оперативную память.

```solidity
pragma solidity ^0.4.19;


contract SandwichFactory {
  struct Sandwich {
    string name;
    string status;
  }

  Sandwich[] sandwiches;

  function eatSandwich(uint _index) public {
    // Сэндвич mySandwich = sandwiches[_index];

    // ^ Вроде все в порядке, но Solidity выдаст предупреждение, 
    // что надо ясно указать `storage` или `memory`.

    // Поэтому используй ключевое слово `storage`, вот так: 
    Sandwich storage mySandwich = sandwiches[_index];
    // ...где `mySandwich` указывает на `sandwiches[_index]` в хранилище, и...
    mySandwich.status = "Eaten!";
    // ...навсегда изменит `sandwiches[_index]` в блокчейне.

    // Если нужна просто копия, используй `memory`:
    Sandwich memory anotherSandwich = sandwiches[_index + 1];
    // ...тогда `anotherSandwich` будет простой копией данных в памяти, таким образом... 
    anotherSandwich.status = "Eaten!";
    // ...всего лишь модифицирует временную переменную и не окажет влияния
    // на `sandwiches[_index + 1]`. Но ты можешь сделать и так... 
    sandwiches[_index + 1] = anotherSandwich;
    // ...если надо сохранить данные в блокчейне.
  }
}
```