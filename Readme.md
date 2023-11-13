

## Sample solutions

I've implemented [quarto profiles](https://quarto.org/docs/projects/profiles.html). To render the book without sample solutions, run `quarto render` or `quarto preview` etc. To show sample solutions, run `quarto render --profile musterloesung`. The profile is defined in `_quarto-musterloesung.yml`.

By default, all code chunks and their outputs are only be visible in the sample solutions. To explicitly show code chunks (and outputs), add `#| echo: true` and `#| output: true`. For sample solutions, use the chunk option `filename` to show a label for the solution.

````
```{r}
#| filename: Musterlösung
1+1
```
````

To display certain text or other content only in the sample solutions, add it in the following manner. 

```
::::{.content-visible when-profile="musterloesung"}
:::{.callout-note}
## Musterlösung

In CH1903+ LV95

:::
::::

```