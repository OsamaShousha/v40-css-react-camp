 1-Todo App – CSS i React
  Jag  kopplas CSS in i React genom att importera "import "./App.css";

  2 -användaren  ser vilka todos som är klara if todo är done 
  eller har värd true då fick todo complete class med style 
  text-decoration: line-through;
  opacity: 0.6;


3- Om stilen inte fungerar

Jag kontrollerar:

Spara filerna.
Kontrollera importen: import "./App.css";
Kontrollera className: att JSX använder rätt klass, till exempel "completed".
Öppna Inspect i webbläsaren och kontrollera elementet och CSS-regeln.


Felsökning

1- Klassen finns, men stilen syns inte

Om jag ser class="completed" i Inspect/Elements men Todo:n inte blir överstruken, kontrollerar jag CSS-regeln och om någon annan regel skriver över den.

Exempel från min app:

```jsx
<li className={t.done ? "completed" : ""} key={t.id}>
  {t.text}
</li>


Om class="completed" inte finns i Inspect, kontrollerar jag className, stavningen och ternary-uttrycket.
Om ingen styling från App.css fungerar alls, kontrollerar jag först importen och sökvägen.
Om importen är fel kan Vite visa ett fel. Jag kontrollerar därför först att App.css finns på rätt plats och att importen är korrekt.
