# fancy-invoice
```cpp
namespace std {
  template<class... Args> void println(const Args&&... args) {
    SetConsoleOutputCP(1252);
    std::locale::global(std::locale(""));
    std::cout.imbue(std::locale());
    (std::cout << ... << args) << '\n';
  }

  template<class... Args> void println(Args&&... args) {
    SetConsoleOutputCP(1252);
    std::locale::global(std::locale(""));
    std::cout.imbue(std::locale());
    (std::cout << ... << std::move(args)) << '\n';
  }
}
```

```auto main()``` ```->``` ```int``` ```{```   
```std::string invoice``` = 
```R```"```(```
    ```{``` 
      ``` "resourceType": ```"[1](https://www.youtube.com/watch?v=Zv1QV6lrc_Y&t=16s)```nvoice```",
      "```id```": "[2](https://www.youtube.com/watch?v=J2Etmui1Rr0&t=1m04s)",
      "```status```": "[3](https://www.youtube.com/watch?v=Ryt2SuHYhW0&t=2m07s)",
      "[4](https://en.wikipedia.org/wiki/Net_worth)": ```{```
        "```value```": "```203.127.527.240```",
        "```currency```": "[5](https://www.xe.com/it/currencyconverter/convert/?Amount=203127527240&From=EUR&To=USD)"
      ```}
      ```
      "```bankAccountDetails```": ```{```
        "```iban```": "```IT90M 0760 10140 00001053478515```"
        "```bic-swift```": "```BPPIITRRXXX```"
      ```}```
    ```}```
  ```)";```
  ```std::println(invoice);```
```}```


