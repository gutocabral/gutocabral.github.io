#### Arduino/C

``` c++
const int botao = 12;
const int led = 7;

int estadoBotao = 0;

void setup() {
  pinMode(led, OUTPUT);
  pinMode(botao, OUTPUT);
}

void loop() {
  while(true) {
    estadoBotao = digitalRead(botao);
    while (estadoBotao == HIGH) {
      digitalWrite(led, HIGH);
      delay(1000);
      digitalWrite(led, LOW);
      delay(1000);
      estadoBotao = digitalRead(botao);
    }
  }
}
```

____

#### HTML

```html
<!DOCTYPE html>
<html>
<head>
    <title>Titulo</title>
    <meta charset="uft-8" />
    <link href="path/to/css.css" rel="stylesheet" />
    <style>
        tag, .class, #id { font-weight: bold; }
    </style>
</head>
<body>
    <form action="envia.php" method="GET">
        <input type="text/password/hidden/color" name="texto" size="15">
        <input type="tel/email/url" name="contato">
        <input type="number/range" name="valor" min="0" max="10">
        <input type="date/month/week/time/datetime" name="tempo">
        <input type="checkbox/radio" name="opcao" value="opcao">
        <input type="submit/image/reset" scr="path/to/(if)_image" value="Enviar">
        <textarea></textarea>
        <select (multiple) name="list">
            <option value="opcao_1">Opção 1
            <option value="opcao_2">Opção 2
        </select>
    </form>
    <article><aside><footer><header><hgroup><nav><section>
</body>
</html>
```

____

#### Servlet

```java
import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;

public class Hello extends HttpServlet {
    public void doGet (HttpServletRequest request, HttpServletResponse response,
                       throws ServletException, IOException) {
        response.setContentType ("text/html");
        PrintWriter out = response.getWriter();
        String nome = request.getParameter("nome");
        out.println ("<HTML>");
        out.println ("<HEAD><TITLE>Olá</TITLE></HEAD>");
        out.println ("<BODY>");
        out.println ("<H1>Hello " + nome + "!</H1>");
        out.println ("</BODY></HTML>");
    }
}
```

____

#### JSP

```HTML
<%@ page (...) >
<%@ include (...) >
<%@ taglib (...) >
<HTML>
<HEAD>
    <TITLE>Olá</TITLE>
</HEAD>
<BODY>
	<% String nome = request.getParameter("nome"); %>
    <H1>Olá <%=nome%>! </H1>
</BODY>
</HTML>
```

