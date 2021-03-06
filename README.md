# Отчёт о тестировании пополнения счёта VIP-клиента.

## Краткое описание

**Дата начала** | **Дата окончания**
------------ | -------------
27.10.2021 | 28.10.2021

Было проведено автотестирование приложения пополнения счёта VIP-клиента.

*На тестирование затрачено:* **1 час**

В результате тестирования выявлены следующие дефекты:

*В процессе проведения пополнения текущего счета VIP клиента, произошел
сбой при выполнении операции. Причиной сбоя послужил некорректный тип
переменной для хранения итогового значения перевода.*


## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты*:
* Приложение Java
```javascript
public class Main {
    public static void main(String[] args) {
        int account = 2_000_000_000;
        int transfer = 500_000_000;
        int totalAccount = account + transfer;
        System.out.println(totalAccount);
    }
}
```

В качестве тестовых данных использовались данные **[изложенные в ДЗ](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/MERGED.md)**:
* Переменная **account** = *2 000 000 000*
* Переменная **transfer** = *500 000 000*
* Переменная **totalAccount** с ожидаемым результатом = **2 500 000 000**

Тестирование производилось в следующем окружении:
* Windows 8.1
* Java 11.0.12
* IntelliJ IDEA 2021.2.3 (Community Edition)
