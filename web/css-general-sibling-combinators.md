# [general sibling combinators](https://www.w3.org/TR/selectors-4/#general-sibling-combinators)



```CSS
.b {
  background-color: blue;
}

.a ~ .b {
  background-color: powderblue;
}
```

```html
<ul>
  <li class="b">1st</li>
  <li class="a">2nd</li>
  <li>3rd</li>
  <li class="b">4th</li>
  <li class="b">5th</li>
</ul>
```

1st will have blue background, 4th and 5th a powderblue background because they follow and element with the `a` class.
