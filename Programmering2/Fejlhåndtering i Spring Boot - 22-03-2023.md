# Fejlhåndtering i Spring Boot - 22-03-2023

- **Fag:** Programmering 2
- **Oprettet:** March 21, 2023 3:11 PM
- **Type:** Forberedelse

# Materialer

[https://www.codejava.net/frameworks/spring-boot/spring-boot-error-handling-guide](https://www.codejava.net/frameworks/spring-boot/spring-boot-error-handling-guide)

# Noter

## Whitelabel Error Page

En whitelabel fejlside er en standard fejlside i Spring Boot, som vises, når en ikke-fanget exception opstår, og ingen anden fejlside er konfigureret. Denne side indeholder en staktrace og andre tekniske detaljer om fejlen, og er normalt ikke brugervenlig. Det er en god ide at konfigurere en tilpasset fejlside, der er mere forståelig for brugeren, og som giver mere specifik information om fejlen.

De mest almindelige HTTP-fejlstatuskoder er 400, 401, 403, 404, 500 og 503.

- 400 Bad Request: Anmodningen kunne ikke forstås af serveren på grund af ugyldig syntaks.
- 401 Unauthorized: Anmodningen kræver godkendelse.
- 403 Forbidden: Serveren kan forstå anmodningen, men nægter at autorisere adgang.
- 404 Not Found: Serveren kunne ikke finde den anmodede ressource.
- 500 Internal Server Error: Serveren stødte på en uventet tilstand, der forhindrede den i at fuldføre anmodningen.
- 503 Service Unavailable: Serveren er midlertidigt ikke i stand til at behandle anmodningen på grund af overbelastning eller vedligeholdelse.

## Fejlhåndtering i Spring Boot

Hvis du vil deaktivere whitelabel error page i Spring Boot, kan du gøre det ved at tilføje følgende linje til `application.properties`-filen:

```
server.error.whitelabel.enabled=false

```

Dette vil deaktivere whitelabel error page og forhindre, at den vises, når der opstår en ikke-fanget exception i din applikation.

Det er muligt at oprette en `error.html` fil i `src/main/resources/templates` mappen for at lave en custom error page i Spring Boot. Denne fil vil blive brugt som standard fejlside for alle fejl i din applikation, medmindre du har konfigureret en anden fejlside for en specifik exception. For mere information om dette emne, kan du se [dette link](https://www.baeldung.com/spring-boot-custom-error-page). Jeg beklager forvirringen i mit tidligere svar.

## Custom Error Handling Controller

```java
package net.codejava;
 
import javax.servlet.RequestDispatcher;
import javax.servlet.http.HttpServletRequest;
 
import org.springframework.boot.web.servlet.error.ErrorController;
import org.springframework.http.HttpStatus;
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.GetMapping;
 
@Controller
public class CustomErrorController  implements ErrorController {
 
    @GetMapping("/error")
    public String handleError(HttpServletRequest request) {
        String errorPage = "error"; // default
         
        Object status = request.getAttribute(RequestDispatcher.ERROR_STATUS_CODE);
         
        if (status != null) {
            Integer statusCode = Integer.valueOf(status.toString());
             
            if (statusCode == HttpStatus.NOT_FOUND.value()) {
                // handle HTTP 404 Not Found error
                errorPage = "error/404";
                 
            } else if (statusCode == HttpStatus.FORBIDDEN.value()) {
                // handle HTTP 403 Forbidden error
                errorPage = "error/403";
                 
            } else if (statusCode == HttpStatus.INTERNAL_SERVER_ERROR.value()) {
                // handle HTTP 500 Internal Server error
                errorPage = "error/500";
                 
            }
        }
         
        return errorPage;
    }
     
    @Override
    public String getErrorPath() {
        return "/error";
    }
}
```
