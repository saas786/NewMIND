---
type: paper
tags: 📥️/📜️/🩳/🗿
aliases:
  - 
cssclass: 
---



# Title: **[[import and inheritance 2021-09-18]]**
- `Type:` [[&]]
- `Links:` 
- `Reviewed Date:` [[2021-09-18]]

## [[inheritance]]

В Solidity есть фича, которая помогает управлять длинными контрактами — **_наследование_**:

```
contract Doge {
  function catchphrase() public returns (string) {
    return "Клевый песик";
  }
}

contract BabyDoge is Doge {
  function anotherCatchphrase() public returns (string) {
    return "Клевый щеночек";
  }
}
```

`BabyDoge` (щенок) **_наследует_** `Doge` (Псу!). Если ты скомпилируешь и развернешь `BabyDoge`, он получит доступ и к `catchphrase()` и к `anotherCatchphrase()` (и ко всем остальным открытым функциям, которые мы опишем в `Doge`).

Это можно использовать для логического наследования (как с подтипами, `Cat` (кошка) это `Animal` (животное)), или для простой организации кода, группируя вместе одинаковую логику внутри различных классов.

---

### import

Когда у тебя несколько файлов и нужно импортировать один в другой, Solidity использует ключевое слово `import`:

```
import "./someothercontract.sol";

contract newContract is SomeOtherContract {

}
```

Если у нас есть файл `someothercontract.sol` в той же директории, что и этот контракт (`/` нам говорит об этом), то компилятор инпортирует его.



### multi # Inheritance
```
contract SatoshiNakamoto is NickSzabo, HalFinney { 
// Omg, the secrets of the universe revealed! 
}
``