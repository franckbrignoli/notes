# Tools

### Beancount

#### Distinct Ledger in Fava

Add a title in each files

```text
option "title" "Personal"
```

Start fava with your multiple files

```text
$ fava file1 file2
```

 And now you can switch in the header

#### SQL 

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

