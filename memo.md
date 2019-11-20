ściąga do gita: 

git status -

git pull

git push

git clone

git add src/

git add .

git checkout -b 'introduce-spring'

git push origin 

git config --global


wkleić do poma dodatkowe linijki springbootowe


---
import org.springframework.web.bind.annotation.RestController;


import org.springframework.web.bind.annotation.RequestMapping;

import java.util.Collections;

import java.util.List;


@RestController


@RequestMapping("/api/cards")


public class CreditCardReportingController {
 CreditCardFacade api;
 @Autowired
 public CreditCardReportingController(CreditCardFacade api){
  this.api = api;
 }

 http://localhost:8080/api/cards/balances
 
 @GetMapping("/balances")
 
 public List<CardBalanceDto> cardsBalances(){
 
    return api.cardsBalances()
    return Array.asList(
      new CardBalanceDto(number: "1234", BigDecimal.valueOf(1000));
      new CardBalanceDto(number: "1543", BigDecimal.valueOf(2000));
      new CardBalanceDto(number: "6578", BigDecimal.valueOf(8000));
     );
  }
  
  
 

  @PostMapping("/withdraw")
  public void withdraw(@RequestBody withdrawCommand command){
      api.withdraw(command);
  }
}
  
  
  ctrl+enter tworzyć nową klasę dla CardBalanceDto
  
  Nowa klasa
  
 
  alt insert - generate setters, getters, constructor
  
  wysyłanie jsona
  
  curl -x POST localhost:8080/api/cards/withdraw -H "Content-Type: apllication/json" -d '{"creditCardNumber": "1234", "valueOf": 2000.10}'
  
  
 Klasa CreditCardConfiguration
 
 @Configuration
  
