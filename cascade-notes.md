The cascade determines which rules actually get applied to our html.
There are multiple (we will look at 3) factors that cascade used:
    1) specificity
    2) Inheritance
    3) Rule Order

1) Specificity:
- a CSS declaration that is more specific will take precedence. 
- Inline styles have the highest specificity, over external and internal. 
- Types of selectors also have specificity levels: ID, then Class, then Type (includes more but we covered these 3 for now)
- when there is multiple selectors of the same type,the rule with the greater number of selectors will take precedence, e.g.: (color:red will take precedence because theres 2 selectors in that class)
<!-- index.html -->
```
<div class="main">
  <div class="list subsection">Red text</div>
</div> 


/* rule 1 */
.subsection {
  color: blue;
}

/* rule 2 */
.main .list {
  color: red;
}
```

- some special symbols for comparing selectors, like universal selector *, +, ~, >, and empty space dont add specificity, they have zero specificity value.

2) Inheritance:
- certain CSS properties, when applied to an element, are inherited by that element's descendents
- typography-based properties (e.g. color, font-size, font-family, etc.) are usually inherited, most other properties arent
- the exception is when directly targeting an element, e.g.: (The parent does have higher specficity because its an ID, but the child element is directly targeted so it would be blue, while red from the parent is only inherited)
```
<!-- index.html -->

<div id="parent">
  <div class="child"></div>
</div>

/* styles.css */

#parent {
  color: red;
}

.child {
  color: blue;
}
```

3) Rule Order:
- tie breaker of tie breakers... after every factor has been applied, if there are still conflicting ruels targeting an element, the *last* rule is the winner