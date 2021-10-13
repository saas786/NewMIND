---
type: paper
tags: 📥️/📜️/🩳/🗿
aliases:
  - 
cssclass: 
---



# Title: **[[interface 2021-09-25]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2021-09-25]]




### inteface
**_интерфейс_** - Спец метод определения функций из других контрактов, с которыми можно взаимодействовать с всеми другими контрактами в блокчейне Ethereum, если они задают функции как `public` (открытые) или `external` (внешние).

Чтобы наш контракт связался с другим контрактом в блокчейне, которым владеем не мы, сначала нужно определить **_интерфейс_**.

Посмотрим простой пример. Допустим, в блокчейне существует такой контракт:
```
contract LuckyNumber {
	mapping(address => uint) numbers; 
	function setNum(uint _num) public { 
		numbers[msg.sender] = _num; 
	} 
	function getNum(address _myAddress) public view returns (uint) {
	return numbers[_myAddress]; 
	}
}
```

Это простой контракт, где каждый может хранить свой счастливый номер, связаный с личным адресом Ethereum. Тогда любой может найти счастливый номер человека по адресу.

Теперь допустим, что у нас есть другой внешний контракт, который хочет считать данные в этом контракте, используя функцию `getNum`.

Сначала нам надо будет определить **_интерфейс_** контракта `LuckyNumber` (счастливый номер):

```
contract NumberInterface {
  function getNum(address _myAddress) public view returns (uint);
}
```

Это похоже на определение контракта, но есть несколько отличий. Во-первых, мы объявляем только те функции, с которыми хотим взаимодействовать - в данном случае `getNum` - и не упоминаем другие функции или переменные состояния.

Во-вторых, мы не определяем тела функций. Вместо фигурных скобок (`{` и `}`) мы заканчиваем задание функции точкой с запятой (`;`).

Это как скелет контракта. Так компилятор узнает, что это интерфейс.


### Взаимодействие 
```
contract NumberInterface {
function getNum(address _myAddress) public view returns (uint); 
}
```

Мы можем использовать его в контракте следующим образом:

```
contract MyContract {
  address NumberInterfaceAddress = 0xab38... 
  // ^ Адрес контракта FavoriteNumber в Ethereum
Number InterfacenumberContract=NumberInterface(NumberInterfaceAddress)
  // Сейчас `numberContract` указывает на другие контракты

  function someFunction() public {
    // Теперь можно вызвать `getNum` из контракта:
    uint num = numberContract.getNum(msg.sender);
    // ...и сделать что-то с `num` здесь
  }
}
```