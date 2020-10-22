# Tools

### Beancount SQL

The VAT that I should pay

```text
SELECT month, sum(cost(position))
WHERE account ~ "Liabilities:Payables:VAT*"
AND NOT description ~ "USt-VZ*"
```

The VAT that I have paid

```text
SELECT  month, position, description
WHERE account ~ "Liabilities:Payables:VAT*"
AND description ~ "USt-VZ*"
```

