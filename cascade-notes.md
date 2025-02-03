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
