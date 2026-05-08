# Custom [Postfix Completion](https://www.jetbrains.com/help/idea/postfix-code-completion.html)

## Java

### assertThat

Applicable expression types:

- non void


- [ ] apply to the topmost expression

```
org.assertj.core.api.Assertions.assertThat($EXPR$).$END$
```

- [x] use static import if possible

### isEqualTo

Applicable expression types:

- non void


- [ ] apply to the topmost expression

```
org.assertj.core.api.Assertions.assertThat($EXPR$).isEqualTo($END$);
```

- [x] use static import if possible

## JavaScript (also works in Typescript)

### tobe

- [ ] apply to the topmost expression

```
expect($EXPR$).toBe($END$)
```

### toeq

```
expect($EXPR$).toBe($END$)
```

### expect

```
expect($EXPR$).$END$
```

### stringify

```
JSON.stringify($EXPR$, null, 2)$END$
```
