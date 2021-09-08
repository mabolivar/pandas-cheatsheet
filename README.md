# pandas-cheatsheet
High quality pandas cheatsheet for data manipulation

### Fast filtering within groups
```python
(df
  .assign(min_time=lambda x: x.groupby(["courier_id", "order_id", "event"]).time.transform("min"))
   [lambda x: x.time == x.min_time]
   .drop(columns=["min_time"])
```

## References

+ [The Most Efficient if-elif-else in Pandas](https://towardsdatascience.com/the-most-efficient-if-elif-else-in-pandas-d4a7d4502d50)
+ [The Unreasonable Effectiveness of Method Chaining in Pandas](https://towardsdatascience.com/the-unreasonable-effectiveness-of-method-chaining-in-pandas-15c2109e3c69)
+ [Using Pandas Method Chaining to improve code readability](https://towardsdatascience.com/using-pandas-method-chaining-to-improve-code-readability-d8517c5626ac)
+ [Pandas Cheat Sheet — Python for Data Science](https://www.dataquest.io/blog/pandas-cheat-sheet/) by [DataQuest](https://www.dataquest.io/)
+ [Data Wrangling with pandas](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf) @ https://pandas.pydata.org/
