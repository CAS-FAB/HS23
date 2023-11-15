

## Sample solutions

I've implemented [quarto profiles](https://quarto.org/docs/projects/profiles.html). To render the book without sample solutions, run `quarto render` or `quarto preview` etc. To show sample solutions, run `quarto render --profile musterloesung`. The profile is defined in `_quarto-musterloesung.yml`. This means, that I don't have to play around with `echo` and `output` in the code chunks.



To display certain text or code content only in the sample solutions, add it in the following manner. 

```
::::{.content-visible when-profile="musterloesung"}
:::{.callout-note}

```{r}
#| filename: Musterlösung
1+1
```

:::
::::

```